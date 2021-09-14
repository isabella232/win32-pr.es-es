---
title: Efecto de pósterización
description: El efecto de pósterización reduce el número de colores únicos en una imagen.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c98c55154300f7b29c23c24e97570335c6e930f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162641"
---
# <a name="posterize-effect"></a>Efecto de pósterización

El efecto de pósterización reduce el número de colores únicos en una imagen.

El CLSID para este efecto es CLSID \_ D2D1Posterize.

-   [Imagen de ejemplo](#example-image)
-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de salida de efecto](images/posterize-effect.png)

## <a name="sample-code"></a>Código de ejemplo


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de pósterización se definen mediante la [**enumeración \_ POSTERIZE \_ PROP de D2D1.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


