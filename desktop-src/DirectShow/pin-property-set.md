---
description: Anclar conjunto de propiedades
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Anclar conjunto de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d143d980de7f2a634deecb2c3f06509854ac5a50fbe120da279cce3ad97be1e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316105"
---
# <a name="pin-property-set"></a>Anclar conjunto de propiedades

El conjunto de propiedades de pin devuelve la categoría de pin para un pin en un filtro. El filtro establece la categoría cuando crea el pin; la categoría indica qué tipo de datos entrega o recibe este pin.



| Etiqueta | Value |
|-------------------|----------------------|
| GUID del conjunto de propiedades | **Anclar AMPROPSETID \_** |



 



| Id. de propiedad                   | Descripción                      |
|-------------------------------|----------------------------------|
| **CATEGORÍA DE PIN DE AMPROPERTY \_ \_** | Especifica la categoría de un pin. |



 

DirectShow define las siguientes categorías de pin en el archivo de encabezado Uuids.h.



| GUID de categoría                     | Descripción                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PIN \_ CATEGORY \_ ANALOGVIDEOIN**  | Pin de entrada del filtro de captura que toma análogo y lo digitaliza.                                                                                                                                                                                                                                                     |
| **CAPTURA DE \_ CATEGORÍA DE \_ PIN**        | Pin de captura.                                                                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ CC**             | Anclar que proporciona datos de subtítulos de la línea 21.                                                                                                                                                                                                                                                                      |
| **PIN \_ CATEGORY \_ EDS**            | Anclar que proporciona Data Services extendidos (línea 21, incluso campos).                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY LA CATEGORÍA DE \_ PIN**          | Anclar que proporciona datos de North American Videotext Standard.                                                                                                                                                                                                                                                                   |
| **VISTA PREVIA \_ DE CATEGORÍA DE \_ PIN**        | Pin de vista previa.                                                                                                                                                                                                                                                                                                            |
| **CATEGORÍA \_ DE PIN \_ TODAVÍA**          | Anclar que proporciona una imagen fija. El pin de captura del filtro debe estar conectado antes de que se conecte el pin de imagen fija.                                                                                                                                                                                                    |
| **PIN \_ CATEGORY \_ TELETEXT**       | Anclar que proporciona teletexto (una variante de subtítulos).                                                                                                                                                                                                                                                                   |
| **CÓDIGO \_ DE TIEMPO DE CATEGORÍA DE \_ PIN**       | Anclar que proporciona datos de código de tiempo.                                                                                                                                                                                                                                                                                            |
| **CATEGORÍA DE PIN \_ \_ VBI**            | Anclar que proporciona datos de intervalo de espacio en blanco vertical.                                                                                                                                                                                                                                                                          |
| **PIN \_ CATEGORY \_ VIDEOPORT**      | Pin de salida de vídeo que se va a conectar al pin de entrada cero en el panel [Superposición Mixer](overlay-mixer-filter.md).                                                                                                                                                                                                                    |
| **CATEGORÍA \_ DE PIN \_ VIDEOPORT \_ VBI** | Anclar para conectarse al asignador de superficie de [VBI,](vbi-surface-allocator.md)el filtro de asignador de superficie de VBI necesario para asignar la memoria de vídeo correcta para cosas como superposiciones de subtítulos en escenarios donde se usa un puerto de vídeo. Los escenarios PCI, IEEE 1394 y USB no usan este filtro. |
| **CAPTURA DE \_ VÍDEO \_ CC DE PINNAME \_**   | Patilla de subtítulos de lalicación de hardware                                                                                                                                                                                                                                                                                  |



 

Esta propiedad es de solo lectura.

### <a name="example-code"></a>Código de ejemplo

El código siguiente muestra cómo comprobar si un pin admite este conjunto de propiedades y, si es así, cómo obtener la categoría pin:


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> En este ejemplo se usa [la función SafeRelease para](../medfound/saferelease.md) liberar punteros de interfaz.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos de anclar para filtros de captura](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> <dt>

[Trabajar con categorías de pin](working-with-pin-categories.md)
</dt> </dl>

 

 
