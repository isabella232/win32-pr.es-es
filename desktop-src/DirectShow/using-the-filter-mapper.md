---
description: Usar el asignador de filtros
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Usar el asignador de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911070"
---
# <a name="using-the-filter-mapper"></a>Usar el asignador de filtros

El [asignador de filtros](filter-mapper.md) es un objeto com que enumera los filtros de DirectShow en función de varios criterios de búsqueda. El asignador de filtros puede ser menos eficaz que el enumerador de dispositivos del sistema, por lo que si necesita filtros de una categoría determinada, debe usar el enumerador de dispositivos del sistema. Pero si necesita buscar un filtro que admita una combinación determinada de tipos de medios, pero no se encuentra en una categoría de borrado, puede que tenga que usar el asignador de filtros. (Un ejemplo sería un filtro de representador o un filtro de descodificador).

El asignador de filtros expone la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) . Para buscar un filtro, llame al método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Este método toma varios parámetros que definen los criterios de búsqueda y devuelve un enumerador para los filtros coincidentes. El enumerador admite la interfaz [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) y proporciona un moniker único para cada filtro coincidente.

En el ejemplo siguiente se enumeran los filtros que aceptan la entrada de vídeo digital (DV) y que tienen al menos un PIN de salida, de cualquier tipo de medio. (El filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) coincide con estos criterios).


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



El método [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) tiene un número bastante grande de parámetros, que se comentan en el ejemplo. Los más importantes para este ejemplo son:

-   Valor de mérito mínimo: el filtro debe tener un valor de mérito por encima del mérito \_ \_ no \_ utilizado.
-   Tipos de entrada: el llamador pasa una matriz que contiene pares de tipos y subtipos principales. Solo coincidirán los filtros que admiten al menos uno de estos pares.
-   Coincidencia exacta: un filtro puede registrar valores **null** para el tipo principal, el subtipo, la categoría de PIN o el medio. A menos que especifique la coincidencia exacta, un valor **null** actúa como carácter comodín, que coincide con cualquier valor que especifique. Con la coincidencia exacta, el filtro debe coincidir exactamente con los criterios. Sin embargo, si se proporciona un parámetro **null** en los criterios de búsqueda, siempre actúa como un carácter comodín o "no tiene cuidado", que coincide con cualquier filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumerar dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Conexión inteligente](intelligent-connect.md)
</dt> </dl>

 

 
