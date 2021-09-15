---
description: Describe cómo inicializar un XPS OM, que permite a un programa crear un documento XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Inicialización de una instancia de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568592"
---
# <a name="initialize-an-xps-om"></a>Inicialización de una instancia de XPS OM

Describe cómo inicializar un XPS OM, que permite a un programa crear un documento XPS.

Las interfaces de la API de documentos XPS se crean mediante una [**interfaz IXpsOMObjectFactory.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) Para obtener un puntero a **IXpsOMObjectFactory** que se puede usar en el programa, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [Tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Ejemplo de código

En el ejemplo siguiente se crea el generador de objetos que se usará para crear interfaces XPS OM en otros ejemplos.


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a>Prácticas recomendadas

Puede hacer que el programa sea más eficaz si obtiene un puntero a una interfaz [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la primera vez que necesita llamar a **IXpsOMObjectFactory** para crear una interfaz y, a continuación, guardar el puntero para usarlo en otras áreas del programa. Cuando el programa ya no necesita el generador de objetos o no lo necesitará durante un tiempo, se puede liberar el puntero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Crear un OM xps en blanco](create-a-blank-xps-om.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Embalaje](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Referencia de LA API del documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
