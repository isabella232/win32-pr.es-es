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
# <a name="syntax-differences"></a><span data-ttu-id="86456-103">Diferencias de sintaxis</span><span class="sxs-lookup"><span data-stu-id="86456-103">Syntax Differences</span></span>

<span data-ttu-id="86456-104">El cambio más aparente a medida que se desplaza entre los lenguajes de programación es el cambio de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="86456-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="86456-105">Considere el método Add del objeto EnhEvents, que se muestra tal y como se declara en tres lenguajes diferentes.</span><span class="sxs-lookup"><span data-stu-id="86456-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

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

<span data-ttu-id="86456-106">Aunque la sintaxis de cada lenguaje expresa el método de forma diferente, la funcionalidad es la misma.</span><span class="sxs-lookup"><span data-stu-id="86456-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="86456-107">En cada lenguaje, el método Add toma los parámetros *Time* y *Name* , y devuelve un objeto EnhEvent.</span><span class="sxs-lookup"><span data-stu-id="86456-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="86456-108">En el ejemplo de C++, el método devuelve el objeto mediante un tercer parámetro de salida, *pval*.</span><span class="sxs-lookup"><span data-stu-id="86456-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="86456-109">Normalmente, la funcionalidad de un objeto COM es la misma en todos los lenguajes de programación.</span><span class="sxs-lookup"><span data-stu-id="86456-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="86456-110">Por este motivo, la documentación de un objeto COM es útil incluso si el objeto está documentado en otro lenguaje de programación que el que está usando.</span><span class="sxs-lookup"><span data-stu-id="86456-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="86456-111">Las descripciones de la funcionalidad, los parámetros y los valores devueltos del objeto son, con pocas excepciones, válidas para todos los lenguajes.</span><span class="sxs-lookup"><span data-stu-id="86456-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="86456-112">Para obtener información sobre cómo convertir la sintaxis de un objeto COM en otro lenguaje de programación, vea [traducir la sintaxis de objetos com para los lenguajes de programación](translating-com-object-syntax-for-programming-languages.md).</span><span class="sxs-lookup"><span data-stu-id="86456-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="86456-113">Las diferencias de sintaxis entre los lenguajes de scripting JavaScript, JScript y VBScript son menos pronunciadas que las diferencias de sintaxis entre los lenguajes de programación mostrados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="86456-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="86456-114">Por ejemplo, considere la función Square tal como se implementa en cada uno de estos tres lenguajes de scripting:</span><span class="sxs-lookup"><span data-stu-id="86456-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="86456-115">Tenga en cuenta que los lenguajes de scripting, a diferencia de los lenguajes de programación, están débilmente tipados.</span><span class="sxs-lookup"><span data-stu-id="86456-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="86456-116">En otras palabras, no es necesario especificar el tipo de datos de un parámetro o un valor devuelto cuando se declara una función.</span><span class="sxs-lookup"><span data-stu-id="86456-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="86456-117">En su lugar, las variables se convierten automáticamente al tipo de datos adecuado.</span><span class="sxs-lookup"><span data-stu-id="86456-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="86456-118">En el caso de VBScript, todas las variables tienen el mismo tipo de datos, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="86456-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="86456-119">La sintaxis de JavaScript y JScript para Square es la misma.</span><span class="sxs-lookup"><span data-stu-id="86456-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="86456-120">JScript es compatible en gran medida con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="86456-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="86456-121">Sin embargo, JScript incluye algunos objetos que no son compatibles actualmente con JavaScript, como **ActiveXObject**, **Enumerator**, **error**, **global** y **VBArray**.</span><span class="sxs-lookup"><span data-stu-id="86456-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="86456-122">Para obtener más información sobre estos objetos, vea la [Referencia del lenguaje JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="86456-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="86456-123">En la superficie, la sintaxis de JavaScript y JScript es similar a la sintaxis de Java.</span><span class="sxs-lookup"><span data-stu-id="86456-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="86456-124">Esta similitud solo es superficial.</span><span class="sxs-lookup"><span data-stu-id="86456-124">This similarity is only superficial.</span></span> <span data-ttu-id="86456-125">El lenguaje Java se desarrolló independientemente de JavaScript y JScript y no está relacionado con ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="86456-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="86456-126">VBScript, por otro lado, es un subconjunto del lenguaje de programación Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="86456-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="86456-127">Por este motivo, la sintaxis de VBScript es un subconjunto de sintaxis de Visual Basic y a menudo es intercambiable con Visual Basic sintaxis.</span><span class="sxs-lookup"><span data-stu-id="86456-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="86456-128">Para obtener información sobre el uso de objetos COM en lenguajes de scripting, vea [scripting con objetos com](scripting-with-com-objects.md).</span><span class="sxs-lookup"><span data-stu-id="86456-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 