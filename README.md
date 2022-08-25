[![Nuget](https://img.shields.io/nuget/v/BidirectionalDictionary)](https://www.nuget.org/packages/BidirectionalDictionary/)
[![License](https://img.shields.io/github/license/iiKuzmychov/BidirectionalDictionary)](https://github.com/iiKuzmychov/BidirectionalDictionary/blob/master/LICENSE.md)

# BidirectionalDictionary

The **bidirectional dictionary** is a dictionary with non-null unique values that provides access to an inverse dictionary.

### Example #1

```cs
using System.Collections.Generic;

var countryCapitalDictionary = new BidirectionalDictionary<string, string>()
{
    ["Italy"] = "Rome",
    ["India"] = "Mumbai",
    ["USA"]   = "Washington, D.C.",
};

var capital = countryCapitalDictionary["Italy"]; // "Rome"
var country = countryCapitalDictionary.Inverse["Rome"]; // "Italy"
```

Also, you can create a read-only instance of a bidirectional dictionary.

### Example #2

```cs
using System.Collections.ObjectModel;

var readOnlyDictionary = new ReadOnlyBidirectionalDictionary<string, string>(countryCapitalDictionary);
var capital            = readOnlyDictionary["Italy"]; // "Rome"
var country            = readOnlyDictionary.Inverse["Rome"]; // "Italy"
```

## License

The project is licensed under the [MIT](https://github.com/iiKuzmychov/BidirectionalDictionary/blob/master/LICENSE.md) license.
