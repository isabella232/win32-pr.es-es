---
title: Combinación de atributos de matriz
description: Los atributos de campo se pueden proporcionar en varias combinaciones siempre que el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se van a transmitir al servidor.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676458"
---
# <a name="combining-array-attributes"></a><span data-ttu-id="663b4-103">Combinación de atributos de matriz</span><span class="sxs-lookup"><span data-stu-id="663b4-103">Combining Array Attributes</span></span>

<span data-ttu-id="663b4-104">Los atributos de campo se pueden proporcionar en varias combinaciones siempre que el código auxiliar pueda usar la información para determinar el tamaño de la matriz y el número de bytes que se van a transmitir al servidor.</span><span class="sxs-lookup"><span data-stu-id="663b4-104">Field attributes can be supplied in various combinations as long as the stub can use the information to determine the size of the array and the number of bytes to transmit to the server.</span></span> <span data-ttu-id="663b4-105">Las relaciones entre los atributos se definen mediante las siguientes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="663b4-105">The relationships between the attributes are defined using the following formulas:</span></span>

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

<span data-ttu-id="663b4-106">Los valores asociados a los atributos deben obedecer varias reglas de sentido común basadas en esas fórmulas.</span><span class="sxs-lookup"><span data-stu-id="663b4-106">The values associated with the attributes must obey several common-sense rules based on those formulas.</span></span> <span data-ttu-id="663b4-107">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="663b4-107">These rules are:</span></span>

-   <span data-ttu-id="663b4-108">No especifique que el \[ [**primer \_**](/windows/desktop/Midl/first-is) \] valor de índice sea menor que cero o que el \[ valor [**Last \_ sea**](/windows/desktop/Midl/last-is) \] mayor que \[ [**Max \_ is**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="663b4-108">Do not specify a \[[**first\_is**](/windows/desktop/Midl/first-is)\] index value smaller than zero or a \[[**last\_is**](/windows/desktop/Midl/last-is)\] value greater than \[[**max\_is**](/windows/desktop/Midl/max-is)\].</span></span>
-   <span data-ttu-id="663b4-109">No especifique un tamaño negativo para una matriz.</span><span class="sxs-lookup"><span data-stu-id="663b4-109">Do not specify a negative size for an array.</span></span> <span data-ttu-id="663b4-110">Defina el primer y el último elemento para que tengan como resultado un valor de longitud de cero o superior.</span><span class="sxs-lookup"><span data-stu-id="663b4-110">Define the first and last elements so that they result in a length value of zero or greater.</span></span> <span data-ttu-id="663b4-111">Defina el \[ valor [**Max \_ is**](/windows/desktop/Midl/max-is) \] para que el tamaño sea cero o superior.</span><span class="sxs-lookup"><span data-stu-id="663b4-111">Define the \[[**max\_is**](/windows/desktop/Midl/max-is)\] value so that the size is zero or greater.</span></span> <span data-ttu-id="663b4-112">Si se invocó MIDL con la opción [**/error**](/windows/desktop/Midl/-error) Bounds \_ check, el código auxiliar genera una excepción cuando el tamaño es menor que cero, o la longitud transmitida es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="663b4-112">If MIDL was invoked with the [**/error**](/windows/desktop/Midl/-error) bounds\_check option, then the stub raises an exception when the size is less than zero, or the transmitted length is less than zero.</span></span>
-   <span data-ttu-id="663b4-113">No use la \[ [**longitud \_**](/windows/desktop/Midl/length-is) \] y el \[ [**último \_ es**](/windows/desktop/Midl/last-is) los \] atributos al mismo tiempo, o el \[ **tamaño \_** y el \] \[ **último \_ son** \] atributos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="663b4-113">Do not use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes at the same time, nor the \[**size\_is**\] and \[**last\_is**\] attributes at the same time.</span></span>

<span data-ttu-id="663b4-114">Debido a la relación de cierre de C entre matrices y punteros, MIDL también permite declarar matrices en listas de parámetros mediante la notación de puntero.</span><span class="sxs-lookup"><span data-stu-id="663b4-114">Because of the close relationship in C between arrays and pointers, MIDL also lets you declare arrays in parameter lists using pointer notation.</span></span> <span data-ttu-id="663b4-115">MIDL trata un parámetro que es un puntero a un tipo como una matriz de ese tipo si el parámetro tiene cualquiera de los atributos que normalmente se asocian a las matrices.</span><span class="sxs-lookup"><span data-stu-id="663b4-115">MIDL treats a parameter that is a pointer to a type as an array of that type if the parameter has any of the attributes commonly associated with arrays.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

<span data-ttu-id="663b4-116">En el ejemplo anterior, los parámetros de matriz y puntero de las funciones fArray6 y fArray7 son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="663b4-116">In the preceding example, the array and pointer parameters in the functions fArray6 and fArray7 are equivalent.</span></span>

 

 