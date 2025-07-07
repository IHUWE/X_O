# X_O
package XandO;

import java.util.Arrays;
import java.util.List;

public class WinChecker {
    private final List<List<Integer>> wins = Arrays.asList(
        Arrays.asList(1, 2, 3),
        Arrays.asList(4, 5, 6),
        Arrays.asList(7, 8, 9),
        Arrays.asList(1, 4, 7),
        Arrays.asList(2, 5, 8),
        Arrays.asList(3, 6, 9),
        Arrays.asList(1, 5, 9),
        Arrays.asList(3, 5, 7)
    );

    public boolean checkWin(Player player) {
        for (List<Integer> combo : wins) {
            if (player.getMoves().containsAll(combo)) {
                return true;
            }
        }
        return false;
    }
}
