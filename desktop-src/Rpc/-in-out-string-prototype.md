---
title: " in, out, prototipo de cadena"
description: El prototipo de función siguiente usa un solo parámetro \ in, out, String \ para las cadenas de entrada y salida.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995360"
---
# <a name="in-out-string-prototype"></a><span data-ttu-id="185bd-103">\[in, out, prototipo de cadena \]</span><span class="sxs-lookup"><span data-stu-id="185bd-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="185bd-104">El prototipo de función siguiente usa un único \[ [**parámetro in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), de [**cadena**](/windows/desktop/Midl/string) \] para las cadenas de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="185bd-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="185bd-105">La cadena contiene primero la entrada del paciente y, a continuación, se sobrescribe con la respuesta del médico, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="185bd-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="185bd-106">Este ejemplo es similar al que emplea una cadena de un solo recuento para la entrada y la salida.</span><span class="sxs-lookup"><span data-stu-id="185bd-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="185bd-107">Como en este ejemplo, el \[ [**atributo \_ size**](/windows/desktop/Midl/size-is) \] determina el número de elementos asignados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="185bd-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="185bd-108">El \[ atributo de [**cadena**](/windows/desktop/Midl/string) \] indica al código auxiliar que llame a **strlen** para determinar el número de elementos transmitidos.</span><span class="sxs-lookup"><span data-stu-id="185bd-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="185bd-109">El cliente asigna toda la memoria antes de la llamada como:</span><span class="sxs-lookup"><span data-stu-id="185bd-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="185bd-110">Tenga en cuenta que la función Analyze ya no debe calcular la longitud de la cadena devuelta tal como lo hacía en el ejemplo de cadena recuento donde no se usó el atributo de **\[ cadena \]** .</span><span class="sxs-lookup"><span data-stu-id="185bd-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="185bd-111">Ahora, el código auxiliar calcula la longitud como se muestra:</span><span class="sxs-lookup"><span data-stu-id="185bd-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 