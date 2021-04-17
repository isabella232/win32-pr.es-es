---
description: Implementación de IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementación de IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677164"
---
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="08120-103">Implementación de IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="08120-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="08120-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="08120-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="08120-105">La interfaz [**IAMErrorLog**](iamerrorlog.md) contiene un único método, [**LogError**](iamerrorlog-logerror.md).</span><span class="sxs-lookup"><span data-stu-id="08120-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="08120-106">Los parámetros del método contienen información sobre el error que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="08120-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="08120-107">El código de error y la cadena de error se definen mediante los servicios de edición de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="08120-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="08120-108">Para obtener una lista de errores, vea [errores de representación](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="08120-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="08120-109">El parámetro *pExtraInfo* contiene un puntero a un tipo Variant que contiene información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="08120-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="08120-110">El tipo de datos y el contenido de la variante dependen del error específico que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="08120-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="08120-111">Por ejemplo, si el error se debe a un nombre de archivo incorrecto, la variante es una cadena con el nombre de archivo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="08120-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="08120-112">Algunos errores no tienen información adicional, por lo que *pExtraInfo* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="08120-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="08120-113">En el código siguiente se muestra cómo probar el miembro **VT** de la variante, que indica el tipo de datos, y cómo dar formato a un mensaje en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="08120-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> <span data-ttu-id="08120-114">No libere la variante a la que apunta</span><span class="sxs-lookup"><span data-stu-id="08120-114">Do not free the VARIANT pointed to by</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="08120-115">.</span><span class="sxs-lookup"><span data-stu-id="08120-115">.</span></span> <span data-ttu-id="08120-116">Además, la variante deja de ser válida una vez devuelto el método, por lo que no se hace referencia a ella más adelante.</span><span class="sxs-lookup"><span data-stu-id="08120-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="08120-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08120-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08120-118">Errores de registro</span><span class="sxs-lookup"><span data-stu-id="08120-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



