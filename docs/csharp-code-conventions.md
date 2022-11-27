# C# Coding Conventions
This guidelines created specialy for NiTiS-Dev's projects

# Naming conventions
There are several naming conventions to consider when writing C# code

In the following examples, any of the guidance pertaining to elements marked `public`
is also applicable when working with `protected` and `protected internal` elements,
all of which are intended to be visible to external callers

## Type Naming
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
