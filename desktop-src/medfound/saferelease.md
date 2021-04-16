---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715500"
---
# <a name="saferelease"></a>SafeRelease


Muchos de los ejemplos de código de esta documentación usan la siguiente función para liberar punteros de interfaz COM.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> Esta función no está definida en un encabezado de SDK. Para usar esta función, debe definirla en su propio código.

 

Esta función libera el puntero *ppT* y lo establece en **null**.

Otra opción es usar una clase de puntero inteligente, como **CComPtr**, que se define en el Active Template Library (ATL).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
