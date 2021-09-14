---
title: Efecto de tabla de búsqueda 3D
description: Una tabla de consulta 3D es un efecto de uso general que se usa para encapsular cualquier efecto de creación de imágenes 1 1 al calcular previamente cómo asigna el efecto las entradas a las salidas de un subconjunto de todos los valores de entrada.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164273"
---
# <a name="3d-lookup-table-effect"></a>Efecto de tabla de búsqueda 3D

Una tabla de consulta 3D es un efecto de uso general que se usa para encapsular cualquier efecto de creación de imágenes 1:1 mediante el cálculo previo de cómo el efecto asigna entradas a salidas para un subconjunto de todos los valores de entrada.

El efecto 3D Lookup Table (LUT) modifica una imagen de entrada mediante el uso del valor de color RGB de la imagen para indexar una textura 3D, donde la textura contiene un valor de salida precalutado de una canalización de efecto arbitrario.

El LUT 3D debe cargarse en un recurso de textura de GPU para que se represente, y esto puede ser costoso en función del tamaño de la textura y las funcionalidades del dispositivo. Los desarrolladores de aplicaciones pueden especificar cuándo pagar este costo mediante el [**recurso ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D. **ID2D1LookupTable3D** tiene los siguientes atributos:

-   Proporciona una representación abstracta del recurso de GPU del LUT 3D.
-   En función de las funcionalidades del dispositivo, se creará una textura 2D o 3D y se rellenará con los datos de LUT proporcionados.
-   Se puede pasar a la propiedad del efecto LUT 3D para la representación.

El CLSID para este efecto es CLSID \_ D2D1LookupTable3D.

-   [Imagen de ejemplo](#example-image)
-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de salida de efecto](images/3dlookuptable-effect.png)

## <a name="sample-code"></a>Código de ejemplo

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de tabla de búsqueda 3D se definen mediante la enumeración [**D2D1 \_ LOOKUPTABLE3D \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
