---
title: Diferencias de sintaxis
description: El cambio más evidente a medida que se mueve entre lenguajes de programación es el cambio en la sintaxis.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253149"
---
# <a name="syntax-differences"></a>Diferencias de sintaxis

El cambio más evidente a medida que se mueve entre lenguajes de programación es el cambio en la sintaxis.

Considere el método Add del objeto EnhEvents, que se muestra como se declara en tres lenguajes diferentes.

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

Aunque la sintaxis de cada lenguaje expresa el método de forma diferente, la funcionalidad es la misma. En cada lenguaje, el método Add toma los parámetros *Time* y *Name* y devuelve un objeto EnhEvent. En el ejemplo de C++, el método devuelve el objeto mediante un tercer parámetro de salida, *pVal*.

Normalmente, la funcionalidad de un objeto COM es la misma en todos los lenguajes de programación. Por este hecho, la documentación de un objeto COM es útil incluso si el objeto está documentado en otro lenguaje de programación que el que está usando. Las descripciones de la funcionalidad, los parámetros y los valores devueltos del objeto son, con pocas excepciones, válidas para todos los lenguajes.

Para obtener información sobre cómo convertir la sintaxis de un objeto COM en otro lenguaje de programación, vea [Translateing COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).

Las diferencias de sintaxis entre los lenguajes de scripting JavaScript, JScript y VBScript son menos marcadas que las diferencias de sintaxis entre los lenguajes de programación mostrados antes. Por ejemplo, considere la función cuadrada tal como se implementa en cada uno de estos tres lenguajes de scripting:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Observe que los lenguajes de scripting, a diferencia de los lenguajes de programación, están débilmente escritos. En otras palabras, no es necesario especificar el tipo de datos de un parámetro o el valor devuelto al declarar una función. En su lugar, las variables se convierten automáticamente al tipo de datos adecuado. En el caso de VBScript, todas las variables son del mismo tipo de datos, **Variant**.

La sintaxis de JavaScript JScript para square es la misma. JScript es compatible en gran medida con JavaScript. Sin embargo, JScript incluye algunos objetos no admitidos actualmente por JavaScript, como **ActiveXObject**, **Enumerator,** **Error**, **Global** y **VBArray**. Para obtener más información sobre estos objetos, vea JScript [Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

En la superficie, la sintaxis de JavaScript JScript se parece a la sintaxis de Java. Esta similitud solo es superficial. El lenguaje Java se desarrolló independientemente de JavaScript y JScript y no está relacionado con ninguno de los dos.

VBScript, por otro lado, es un subconjunto del Visual Basic programación. Debido a esto, la sintaxis de VBScript es un subconjunto de Visual Basic sintaxis y a menudo es intercambiable con Visual Basic sintaxis.

Para obtener información sobre el uso de objetos COM en lenguajes de scripting, vea [Scripting con objetos COM](scripting-with-com-objects.md).

 

 