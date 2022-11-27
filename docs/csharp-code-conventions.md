# C# Coding Conventions
This guidelines created specialy for NiTiS-Dev's projects

# Naming conventions
There are several naming conventions to consider when writing C# code

In the following examples, any of the guidance pertaining to elements marked `public`
is also applicable when working with `protected` and `protected internal` elements,
all of which are intended to be visible to external callers

## Type naming
Use "PascalCase" when naming types (`class`, `struct`, `delegate`, `record`, `interface`)

```cs
public class DeflateStream : Stream
{
}
```
```cs
public struct Position
{
}
```

Use "PascalCase" when naming record elements
```cs
// Shorty form (1..3 elements)
public record PlayerData(int Id, string Username) {}

// Full form (4 and more elements)
public record PlayerBigData(
  int Id,
  string Username,
  Color UsernameColour,
  MD5 PasswordHash
  ) {}
```

When naming an `interface` insert letter `I` at begining for better interface indication
```cs
public interface ISelectableObject
{
}
```

## Fields naming
Use "PascalCase" when naming `public static`, `public readonly`, `public static readonly` fields and `const`
```cs
public class DontLookAtMe
{
  public readonly string Name;
  public static string HoRedTeDais;
  public static readonly string HoRedToRaze;
  public const string Yera = "2022";
}
```

Use "camelCase" when naming non-public fields and editable non-static `public` fields
```cs
public class DataManager
{
  public string serverUri;
  private string password;
  private readonly int port;
}
```
## Local variable naming
Use "camelCase"
```cs
public class A
{
  public static void B()
  {
    string camelCase;
    int id;
    uint UserId;
  }
}
```
## Parameter naming

Use "camelCase" when naming parameters
```cs
public static class ABVGDEYOZJE
{
  public static void SomeMethod(int index, uint numero, Scene stage, ReplicaType replicaType);
}
```

Use "PascalCase" with T at the begining or "SCREAMING_SNAKE_CASE" when naming generic parameters
```cs
// PascalCase
public class Group<TElement> {}
// SCREAMING_SHAKE_CASE
public class Group<ELEMENT> {}
```

# Layout conventions
Good layout uses formatting to emphasize the structure of your code and to make the code easier to read  
There are several examples of good conventions:
+ Use tabs instead of 4 space
+ Write no more one statement per line
```cs
actor.Ask();
actor.JumpToTheCosmos();
```
+ Declare only same-type variables per line
```cs
int x, y, z;
string name;
```
```cs
int x = 1,
    y = 2,
    z = 4;
string name = "VILYAM";
```
+ Add at least one blank line between method definitions and property definitions
+ Use parentheses to make clauses in an expression apparent, as shown in the following code

