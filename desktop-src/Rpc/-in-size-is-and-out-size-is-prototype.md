---
title: " en, size_is y out, size_is prototipo"
description: El prototipo de función siguiente usa dos cadenas contadas. El desarrollador debe escribir código en el cliente y en el servidor para realizar un seguimiento de las longitudes de la matriz de caracteres y pasar parámetros que indiquen el número de elementos de la matriz que se van a transmitir.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421293"
---
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="8d7eb-104">\[en, el tamaño \_ es \] y \[ fuera, el tamaño \_ es \] prototipo</span><span class="sxs-lookup"><span data-stu-id="8d7eb-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="8d7eb-105">El prototipo de función siguiente usa dos cadenas contadas.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="8d7eb-106">El desarrollador debe escribir código en el cliente y en el servidor para realizar un seguimiento de las longitudes de la matriz de caracteres y pasar parámetros que indiquen el número de elementos de la matriz que se van a transmitir.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="8d7eb-107">Tenga en cuenta que los parámetros que describen la longitud de la matriz se transmiten en la misma dirección que las matrices: *cbIn* y *achIn* están \[ [**en**](/windows/desktop/Midl/in) \] parámetros mientras que *pcbOut* y *achOut* son parámetros de \[ [**salida**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="8d7eb-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="8d7eb-108">Como parámetro **\[ out \]** , el parámetro *pcbOut* debe seguir la Convención de C y declararse como un puntero.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="8d7eb-109">El código de cliente cuenta el número de caracteres de la cadena, incluido el cero final, antes de llamar al procedimiento remoto, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="8d7eb-110">El procedimiento remoto en el servidor proporciona la longitud del búfer de retorno en *cbOut* , como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="8d7eb-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

<span data-ttu-id="8d7eb-111">El \[ atributo de **cadena** \] se puede usar cuando se sabe que un parámetro es una cadena.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="8d7eb-112">Este atributo dirige el código auxiliar para calcular el tamaño de la cadena, lo que elimina la sobrecarga asociada con la longitud de los \[ [](/windows/desktop/Midl/size-is) \] parámetros.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="8d7eb-113">Además, dirigirá el código auxiliar para comprobar que la cadena está terminada en **null** antes de pasar el parámetro a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8d7eb-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 