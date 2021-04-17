---
description: En este tema se describen los requisitos para implementar un PIN de salida en un filtro de captura de DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Requisitos de PIN para los filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686308"
---
# <a name="pin-requirements-for-capture-filters"></a>Requisitos de PIN para los filtros de captura

En este tema se describen los requisitos para implementar un PIN de salida en un filtro de captura de DirectShow.

## <a name="pin-name"></a>Nombre del pin

Puede asignar un nombre a un PIN. Si el nombre del anclaje comienza con el carácter de tilde (~), el administrador de gráficos de filtro no representará automáticamente ese pin cuando una aplicación llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Por ejemplo, si el filtro tiene un PIN de captura y un PIN de vista previa, puede asignarles el nombre "~ Capture" y "Preview", respectivamente. Si una aplicación representa ese filtro en un gráfico, el PIN de vista previa se conectará a su representador predeterminado y no se conectará nada al pin de captura, que es un comportamiento predeterminado razonable. Esto también se puede aplicar a los PIN que proporcionan datos informativos que no están diseñados para ser representados o PIN que necesitan propiedades personalizadas establecidas. Tenga en cuenta que la aplicación puede seguir conectando manualmente los pin con el prefijo de tilde (~).

## <a name="pin-category"></a>Categoría de PIN

Un filtro de captura siempre tiene un PIN de captura y puede tener un PIN de vista previa. Algunos filtros de captura pueden tener otros PIN de salida para ofrecer otros tipos de datos, como la información de control. Cada terminal de salida debe exponer la interfaz [**IKsPropertySet**](ikspropertyset.md) . Las aplicaciones usan esta interfaz para determinar la categoría del PIN. El PIN normalmente devuelve la \_ vista previa de la \_ captura de categoría de PIN o de la categoría de PIN \_ \_ . Para obtener más información, vea [conjunto de propiedades de PIN](pin-property-set.md).

En el ejemplo siguiente se muestra cómo implementar [**IKsPropertySet**](ikspropertyset.md) para devolver la categoría PIN en un PIN de captura:


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

 

 



