---
description: Conjunto de propiedades de PIN
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Conjunto de propiedades de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422840"
---
# <a name="pin-property-set"></a>Conjunto de propiedades de PIN

El conjunto de propiedades PIN devuelve la categoría PIN de un PIN en un filtro. La categoría se establece mediante el filtro cuando crea el PIN; la categoría indica el tipo de datos que el PIN envía o recibe.



|                   |                      |
|-------------------|----------------------|
| GUID del conjunto de propiedades | **AMPROPSETID \_ PIN** |



 



| Id. de propiedad                   | Descripción                      |
|-------------------------------|----------------------------------|
| **\_categoría AMPROPERTY PIN \_** | Especifica la categoría de un PIN. |



 

DirectShow define las siguientes categorías de PIN en el archivo de encabezado UUID. h.



| GUID de categoría                     | Descripción                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PIN \_ categoría \_ ANALOGVIDEOIN**  | PIN de entrada del filtro de captura que toma el analógico y lo digitaliza.                                                                                                                                                                                                                                                     |
| **\_captura de categoría de PIN \_**        | PIN de captura.                                                                                                                                                                                                                                                                                                            |
| **Categoría de PIN \_ \_ CC**             | PIN que proporciona datos de subtítulos (CC) de la línea 21.                                                                                                                                                                                                                                                                      |
| **Categoría de PIN \_ \_ EDS**            | PIN que proporciona Data Services extendida (línea 21, pares campos).                                                                                                                                                                                                                                                            |
| **PIN \_ categoría \_ NABTS**          | PIN que proporciona datos estándar de videotexto de Norteamérica.                                                                                                                                                                                                                                                                   |
| **\_vista previa de categoría de PIN \_**        | PIN de vista previa.                                                                                                                                                                                                                                                                                                            |
| **Categoría de PIN \_ \_ todavía**          | PIN que proporciona una imagen fija. El PIN de captura del filtro debe estar conectado antes de que se conecte el PIN de imagen fija.                                                                                                                                                                                                    |
| **\_teletexto de categoría de PIN \_**       | PIN que proporciona teletexto (una variante de subtítulos).                                                                                                                                                                                                                                                                   |
| **código de tiempo de \_ categoría de PIN \_**       | PIN que proporciona datos de código de tiempo.                                                                                                                                                                                                                                                                                            |
| **PIN \_ categoría \_ VBI**            | PIN que proporciona datos de intervalo de espacio en blanco vertical.                                                                                                                                                                                                                                                                          |
| **videopuerto de categoría de PIN \_ \_**      | PIN de salida de vídeo que se va a conectar a la clavija de entrada cero en el [mezclador de superposición](overlay-mixer-filter.md).                                                                                                                                                                                                                    |
| **Categoría de PIN de \_ \_ videopuerto \_ VBI** | PIN que se va a conectar al [asignador de superficie de VBI](vbi-surface-allocator.md), el filtro de asignador de superficie de VBI necesario para asignar la memoria de vídeo correcta para elementos como superposiciones de subtítulos (CC) en escenarios en los que se usa un puerto de vídeo. Los escenarios PCI, IEEE 1394 y USB no usan este filtro. |
| **\_captura de \_ CC de vídeo PINNAME \_**   | División de hardware cerrado: PIN de subtítulos                                                                                                                                                                                                                                                                                  |



 

Esta propiedad es de solo lectura.

### <a name="example-code"></a>Código de ejemplo

En el código siguiente se muestra cómo comprobar si un PIN admite este conjunto de propiedades y, en ese caso, cómo obtener la categoría de PIN:


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
> En este ejemplo se usa la función [SafeRelease](../medfound/saferelease.md) para liberar punteros de interfaz.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos de PIN para los filtros de captura](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> <dt>

[Trabajar con categorías de PIN](working-with-pin-categories.md)
</dt> </dl>

 

 
