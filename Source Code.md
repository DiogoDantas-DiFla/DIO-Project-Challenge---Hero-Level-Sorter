# Source Code

```
import javax.swing.*;

public class HeroLevelSorter {

    public static void main(String[] args) {
        // Name input
        String heroName = JOptionPane.showInputDialog("What is the name of the hero?");
        while (heroName.isBlank()) {
            JOptionPane.showMessageDialog(null, "Please, insert a name", "Empty Field", JOptionPane.ERROR_MESSAGE);
            heroName = JOptionPane.showInputDialog("What is the name of the hero?");
        }

        // Experience (XP) input
        String literalXP = JOptionPane.showInputDialog("What is your XP?");
        while (literalXP.isBlank() || !literalXP.matches("[0-9]+")) {
            JOptionPane.showMessageDialog(null, "Please, insert a number with no letters", "Empty Field", JOptionPane.ERROR_MESSAGE);
            literalXP = JOptionPane.showInputDialog("What is your XP?");
        }
        int numericXP = Integer.parseInt(literalXP);

        // This is where the magic happen
        if (numericXP < 1000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Iron level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else if (numericXP > 1001 && numericXP < 2000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Bronze level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else if (numericXP > 2001 && numericXP < 5000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Silver level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else if (numericXP > 5001 && numericXP < 7000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Gold level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else if (numericXP > 7001 && numericXP < 8000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Platinum level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else if (numericXP > 8001 && numericXP < 9000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Ascending level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else if (numericXP > 9001 && numericXP < 10000) {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Imortal level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        } else {
            JOptionPane.showMessageDialog(null, "The Hero named " + heroName + " is at Radiant level",
                    "Hero Level", JOptionPane.PLAIN_MESSAGE);
        }
    }

}
```