Hassan Moharram 40158285

1.

- p=T: a=T, b,c=T
- p=F: a=F, b,c=F

CC:

| a | b | c | p |
|---|---|---|---|
| T | T | T | T |
| T | T | F | T |
| T | F | T | T |
| T | F | F | F |
| F | T | T | F |
| F | T | F | F |
| F | F | T | F |
| F | F | F | F |

CACC:

| a | b | c | p |
|---|---|---|---|
| T | T | T | T |
| T | T | F | T |
| T | F | T | T |
| T | F | F | F |
| F | T | T | F |
| F | T | F | F |
| F | F | T | F |
| F | F | F | F |

RACC:

| b | c | p |
|---|---|---|
| T | T | T |
| T | F | T |
| F | T | T |
| T | T | F |
| T | F | F |
| F | T | F |

  import static org.junit.Assert.assertEquals;
import org.junit.Test;

public class CheckItTest {

   @Test
   public void testPTrue() {
      assertEquals("P is true", CheckIt.checkIt(true, true, true));
      assertEquals("P is true", CheckIt.checkIt(true, true, false));
      assertEquals("P is true", CheckIt.checkIt(true, false, true));
   }

   @Test
   public void testPFalse() {
      assertEquals("P isn't true", CheckIt.checkIt(false, true, true));
      assertEquals("P isn't true", CheckIt.checkIt(false, false, true));
      assertEquals("P isn't true", CheckIt.checkIt(false, false, false));
   }
}
