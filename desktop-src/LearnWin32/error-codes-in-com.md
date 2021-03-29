---
title: Códigos de error en COM
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790191"
---
# <a name="error-codes-in-com"></a>Códigos de error en COM

Para indicar si se ha realizado correctamente o no, las funciones y los métodos COM devuelven un valor de tipo **HRESULT**. Un **valor HRESULT** es un entero de 32 bits. El bit de orden superior de **HRESULT** indica que el resultado es correcto o incorrecto. Cero (0) indica que se ha realizado correctamente y 1 indica un error.

Esto produce los siguientes intervalos numéricos:

-   Códigos de éxito: 0X0 – 0x7FFFFFFF.
-   Códigos de error: 0x80000000 – 0xFFFFFFFF.

Un número pequeño de métodos COM no devuelve un valor **HRESULT** . Por ejemplo, los métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) devuelven valores Long sin signo. Pero todos los métodos COM que devuelven un código de error lo hace devolviendo un valor **HRESULT** .

Para comprobar si un método COM se realiza correctamente, examine el bit de orden superior del **HRESULT** devuelto. Los encabezados de Windows SDK proporcionan dos macros que facilitan esta tarea: la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) y la macro [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . La macro **Succeeded** devuelve **true** si un **valor HRESULT** es un código de operación correcta y **false** si es un código de error. En el ejemplo siguiente se comprueba si [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) se realiza correctamente.


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



A veces resulta más cómodo probar la condición inversa. La macro [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) hace lo contrario de [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded). Devuelve **true** para un código de error y **false** para un código de éxito.


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



Más adelante en este módulo, veremos algunos consejos prácticos sobre cómo estructurar el código para controlar los errores de COM. (Vea [control de errores en com](error-handling-in-com.md)).

## <a name="next"></a>Siguientes

[Crear un objeto en COM](creating-an-object-in-com.md)

 

 