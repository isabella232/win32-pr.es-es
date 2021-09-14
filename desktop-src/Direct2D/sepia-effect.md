---
title: Efecto sepia
description: Convierte una imagen a tonos sepia.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162593"
---
# <a name="sepia-effect"></a>Efecto sepia

Convierte una imagen a tonos sepia.

El CLSID para este efecto es CLSID \_ D2D1Sepia.

-   [Imagen de ejemplo](#example-image)
-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de salida de efecto](images/sepia-effect.png)

## <a name="sample-code"></a>Código de ejemplo


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto sepia se definen mediante la [**enumeración \_ SEPIA \_ PROP de D2D1.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




