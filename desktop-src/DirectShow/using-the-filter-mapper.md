---
description: Uso del asignador de filtros
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Uso del asignador de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48758c40b97477200b4fab1215eaccac53823771add86d6a8b915370776495a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049624"
---
# <a name="using-the-filter-mapper"></a>Uso del asignador de filtros

El [Asignador de filtros](filter-mapper.md) es un objeto COM que enumera los DirectShow basados en varios criterios de búsqueda. El Asignador de filtros puede ser menos eficaz que el enumerador de dispositivos del sistema, por lo que si necesita filtros de una categoría determinada, debe usar el enumerador de dispositivos del sistema. Sin embargo, si necesita buscar un filtro que admita una determinada combinación de tipos de medios, pero no se encuentre en una categoría sin formato, es posible que tenga que usar el Asignador de filtros. (Un ejemplo sería un filtro de representador o un filtro descodificador).

El Asignador de filtros expone la [**interfaz IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) Para buscar un filtro, llame al [**método IFilterMapper2::EnumMatchingFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) Este método toma varios parámetros que definen los criterios de búsqueda y devuelve un enumerador para los filtros correspondientes. El enumerador admite la [**interfaz IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) y proporciona un moniker único para cada filtro correspondiente.

En el ejemplo siguiente se enumeran los filtros que aceptan la entrada de vídeo digital (DV) y tienen al menos un pin de salida, de cualquier tipo de medio. (El [filtro descodificador de vídeo DV](dv-video-decoder-filter.md) coincide con estos criterios).


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



El [**método EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) tiene un número bastante grande de parámetros, que se comentan en el ejemplo. Entre los importantes de este ejemplo se incluyen:

-   Valor mínimo de meritorio: el filtro debe tener un valor de meritorio por encima de LA PROPIEDAD \_ \_ NO \_ USE.
-   Tipos de entrada: el autor de la llamada pasa una matriz que contiene pares de tipos principales y subtipos. Solo coincidirán los filtros que admiten al menos uno de estos pares.
-   Coincidencia exacta: un filtro puede registrar **valores NULL** para el tipo principal, el subtipo, la categoría pin o el medio. A menos que especifique la coincidencia exacta, un **valor NULL** actúa como un carácter comodín, que coincide con cualquier valor que especifique. Con la coincidencia exacta, el filtro debe coincidir exactamente con los criterios. Sin embargo, si se da un parámetro **NULL** en los criterios de búsqueda, siempre actúa como un valor comodín o "no importa" y coincide con cualquier filtro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración de dispositivos y filtros](enumerating-devices-and-filters.md)
</dt> <dt>

[Inteligencia Conectar](intelligent-connect.md)
</dt> </dl>

 

 
