---
title: Diferencias de sintaxis
description: El cambio más aparente a medida que se desplaza entre los lenguajes de programación es el cambio de sintaxis.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488338"
---
# <a name="syntax-differences"></a>Diferencias de sintaxis

El cambio más aparente a medida que se desplaza entre los lenguajes de programación es el cambio de sintaxis.

Considere el método Add del objeto EnhEvents, que se muestra tal y como se declara en tres lenguajes diferentes.

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

Aunque la sintaxis de cada lenguaje expresa el método de forma diferente, la funcionalidad es la misma. En cada lenguaje, el método Add toma los parámetros *Time* y *Name* , y devuelve un objeto EnhEvent. En el ejemplo de C++, el método devuelve el objeto mediante un tercer parámetro de salida, *pval*.

Normalmente, la funcionalidad de un objeto COM es la misma en todos los lenguajes de programación. Por este motivo, la documentación de un objeto COM es útil incluso si el objeto está documentado en otro lenguaje de programación que el que está usando. Las descripciones de la funcionalidad, los parámetros y los valores devueltos del objeto son, con pocas excepciones, válidas para todos los lenguajes.

Para obtener información sobre cómo convertir la sintaxis de un objeto COM en otro lenguaje de programación, vea [traducir la sintaxis de objetos com para los lenguajes de programación](translating-com-object-syntax-for-programming-languages.md).

Las diferencias de sintaxis entre los lenguajes de scripting JavaScript, JScript y VBScript son menos pronunciadas que las diferencias de sintaxis entre los lenguajes de programación mostrados anteriormente. Por ejemplo, considere la función Square tal como se implementa en cada uno de estos tres lenguajes de scripting:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Tenga en cuenta que los lenguajes de scripting, a diferencia de los lenguajes de programación, están débilmente tipados. En otras palabras, no es necesario especificar el tipo de datos de un parámetro o un valor devuelto cuando se declara una función. En su lugar, las variables se convierten automáticamente al tipo de datos adecuado. En el caso de VBScript, todas las variables tienen el mismo tipo de datos, **Variant**.

La sintaxis de JavaScript y JScript para Square es la misma. JScript es compatible en gran medida con JavaScript. Sin embargo, JScript incluye algunos objetos que no son compatibles actualmente con JavaScript, como **ActiveXObject**, **Enumerator**, **error**, **global** y **VBArray**. Para obtener más información sobre estos objetos, vea la [Referencia del lenguaje JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

En la superficie, la sintaxis de JavaScript y JScript es similar a la sintaxis de Java. Esta similitud solo es superficial. El lenguaje Java se desarrolló independientemente de JavaScript y JScript y no está relacionado con ninguno de ellos.

VBScript, por otro lado, es un subconjunto del lenguaje de programación Visual Basic. Por este motivo, la sintaxis de VBScript es un subconjunto de sintaxis de Visual Basic y a menudo es intercambiable con Visual Basic sintaxis.

Para obtener información sobre el uso de objetos COM en lenguajes de scripting, vea [scripting con objetos com](scripting-with-com-objects.md).

 

 