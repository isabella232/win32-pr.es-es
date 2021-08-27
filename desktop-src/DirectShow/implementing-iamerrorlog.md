---
description: Implementación de IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementación de IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378d48ec9047da6068e8d95143f8b10b7016faea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465242"
---
# <a name="implementing-iamerrorlog"></a>Implementación de IAMErrorLog

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

La [**interfaz IAMErrorLog**](iamerrorlog.md) contiene un único método, [**LogError**](iamerrorlog-logerror.md). Los parámetros del método contienen información sobre el error que se ha producido.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



El código de error y la cadena de error se definen mediante DirectShow Editing Services. Para obtener una lista de errores, vea [Errores de representación.](rendering-errors.md)

El *parámetro pExtraInfo* contiene un puntero a un tipo VARIANT que contiene información adicional sobre el error. El tipo de datos y el contenido de VARIANT dependen del error específico que se produjo. Por ejemplo, si el error se debe a un nombre de archivo incorrecto, VARIANT es una cadena con el nombre de archivo incorrecto. Algunos errores no tienen información adicional, por lo *que pExtraInfo* podría ser **NULL.** El código siguiente muestra cómo probar el miembro **vt** de VARIANT, que indica el tipo de datos, y dar formato a un mensaje en consecuencia.


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
> No liberar la VARIANTE a la que apunta
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>pExtraInfo</code></pre> | 

>
> 
>
> . Además, VARIANT deja de ser válido después de que el método vuelva, por lo que no haga referencia a él más adelante.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de registro](logging-errors.md)
</dt> </dl>

 

 



