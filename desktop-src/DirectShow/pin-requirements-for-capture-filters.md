---
description: En este tema se describen los requisitos para implementar un pin de salida en un filtro DirectShow captura.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Requisitos de anclar filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e72c74f06970bf6124d0e5dffea458bb41bcd0a19db44acc71a51615aa2fee8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316115"
---
# <a name="pin-requirements-for-capture-filters"></a>Requisitos de anclar filtros de captura

En este tema se describen los requisitos para implementar un pin de salida en un filtro DirectShow captura.

## <a name="pin-name"></a>Nombre del pin

Puede dar un nombre a un pin. Si el nombre del pin comienza con el carácter de tilde (~), filter Graph Manager no representa automáticamente ese pin cuando una aplicación llama a [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Por ejemplo, si el filtro tiene un pin de captura y un pin de vista previa, podría nombrarlos "~Capture" y "Preview", respectivamente. Si una aplicación representa ese filtro en un gráfico, el pin de vista previa se conectará a su representador predeterminado y nada se conectará al pin de captura, que es un comportamiento predeterminado razonable. Esto también se puede aplicar a los pines que proporcionan datos informativos que no están diseñados para representarse, o a los pines que necesitan establecer propiedades personalizadas. Tenga en cuenta que la aplicación todavía puede conectar manualmente los pines con el prefijo de tilde (~).

## <a name="pin-category"></a>Categoría de anclar

Un filtro de captura siempre tiene un pin de captura y puede tener un pin de vista previa. Algunos filtros de captura pueden tener otros pines de salida para entregar otros tipos de datos, como la información de control. Cada pin de salida debe exponer la [**interfaz IKsPropertySet.**](ikspropertyset.md) Las aplicaciones usan esta interfaz para determinar la categoría de pin. Normalmente, el pin devuelve PIN \_ CATEGORY CAPTURE o PIN CATEGORY \_ \_ \_ PREVIEW. Para obtener más información, vea [Anclar conjunto de propiedades](pin-property-set.md).

En el ejemplo siguiente se muestra cómo implementar [**IKsPropertySet para**](ikspropertyset.md) devolver la categoría pin en un pin de captura:


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



