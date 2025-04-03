class Solution {
public:
    int longestConsecutive(vector<int>& nums) {
        unordered_map<int, int> map;
        int longestStreak = 0;

        for (int num : nums) {
            if (map.find(num) == map.end()) {
                int left, right;

                if (map.find(num - 1) != map.end()) {
                    left = map[num - 1];
                } else {
                    left = 0;
                }

                if (map.find(num + 1) != map.end()) {
                    right = map[num + 1];
                } else {
                    right = 0;
                }

                int sequenceLength = left + 1 + right;

                map[num] = sequenceLength;

                if (left > 0) {
                    map[num - left] = sequenceLength;
                }

                if (right > 0) {
                    map[num + right] = sequenceLength;
                }

                if (sequenceLength > longestStreak) {
                    longestStreak = sequenceLength;
                }
            }
        }

        return longestStreak;
    }
};
