---
title: Códigos de error en COM
description: Códigos de error en COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dd61208c9ae825999ec0dec024a8cc492b81cae426b1cc4143d694034204d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388293"
---
# <a name="error-codes-in-com"></a>Códigos de error en COM

Para indicar que se ha hecho correctamente o no, los métodos COM y las funciones devuelven un valor de tipo **HRESULT**. Un **valor HRESULT** es un entero de 32 bits. El bit de orden superior del **valor HRESULT** indica que se ha hecho correctamente o no. Cero (0) indica que se ha hecho correctamente y 1 indica error.

Esto genera los siguientes intervalos numéricos:

-   Códigos de éxito: 0x0–0x7FFFFFFF.
-   Códigos de error: 0x80000000–0xFFFFFFFF.

Un pequeño número de métodos COM no devuelve un **valor HRESULT.** Por ejemplo, los [**métodos AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**y Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) devuelven valores long sin signo. Pero todos los métodos COM que devuelven un código de error lo hace devolviendo un **valor HRESULT.**

Para comprobar si un método COM se realiza correctamente, examine el bit de orden superior del **HRESULT devuelto.** Los Windows SDK proporcionan dos macros que facilitan esta tarea: la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) y la [**macro FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) La **macro SUCCEEDED** devuelve **TRUE si** un **HRESULT** es un código correcto y **FALSE** si es un código de error. En el ejemplo siguiente se comprueba [**si CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) se realiza correctamente.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



A veces resulta más cómodo probar la condición inversa. La [**macro FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) hace lo contrario que [**SUCCEEDED.**](/windows/desktop/api/winerror/nf-winerror-succeeded) Devuelve **TRUE para** un código de error y **FALSE para** un código correcto.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



Más adelante en este módulo, se verán algunos consejos prácticos sobre cómo estructurar el código para controlar los errores COM. (Vea [Control de errores en COM).](error-handling-in-com.md)

## <a name="next"></a>Siguientes

[Crear un objeto en COM](creating-an-object-in-com.md)

 

 
