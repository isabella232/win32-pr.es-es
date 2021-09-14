---
title: Efecto de borde
description: Use el efecto de borde para extender una imagen desde los bordes.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- efecto de borde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164226"
---
# <a name="border-effect"></a>Efecto de borde

Use el efecto de borde para extender una imagen desde los bordes. Puede usar este efecto para repetir los píxeles de los bordes de la imagen, ajustar los píxeles del extremo opuesto de la imagen o reflejar los píxeles en el borde del mapa de bits para ampliar la región del mapa de bits.

El CLSID para este efecto es CLSID \_ D2D1Border.

## <a name="example-images"></a>Imágenes de ejemplo

En los ejemplos siguientes se muestra la salida del efecto de borde mediante cada modo. El tamaño de salida es infinito, pero estas imágenes de ejemplo se recortan al doble del tamaño.

### <a name="mirror"></a>Reflejo



| Antes                                                    |
|-----------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto.](images/border-before.jpg) |
| Después                                                     |
| ![Captura de pantalla que muestra la imagen después de la transformación.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Antes                                                        |
|---------------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto de una fijación.](images/border-before.jpg)     |
| Después                                                         |
| ![Captura de pantalla que muestra la imagen después de la transformación para una fijación.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Encapsulado



| Antes                                                       |
|--------------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto de un ajuste.](images/border-before.jpg)    |
| Después                                                        |
| ![Captura de pantalla que muestra la imagen después de la transformación para un ajuste.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                  | Descripción                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modo perimetral X<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ X<br/> | Modo perimetral en la dirección X para el efecto. Puede establecerlo en fijación, encapsulado o reflejo. Consulte [Modos perimetrales](#edge-modes) para obtener más información.<br/> El tipo es D2D1 \_ BORDER \_ EDGE \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ EDGE MODE \_ \_ CLAMP.<br/> |
| Modo perimetral Y<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ Y<br/> | Modo perimetral en la dirección Y del efecto. Puede establecerlo en fijación, encapsulado o reflejo. Consulte [Modos perimetrales](#edge-modes) para obtener más información.<br/> El tipo es D2D1 \_ BORDER \_ EDGE \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ EDGE MODE \_ \_ CLAMP.<br/> |



 

## <a name="edge-modes"></a>Modos perimetrales



| Enumeración de nombre para mostrar e índice                            | Descripción                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> FIJACIÓN DEL MODO PERIMETRAL DE BORDE D2D1 \_ \_ \_ \_<br/>   | Repite los píxeles de los bordes de la imagen.      |
| Encapsulado<br/> AJUSTE DEL MODO PERIMETRAL DE BORDE D2D1 \_ \_ \_ \_<br/>     | Usa píxeles del borde final opuesto de la imagen. |
| Reflejo<br/> REFLEJO DEL MODO PERIMETRAL DE BORDE D2D1 \_ \_ \_ \_<br/> | Refleja píxeles sobre el borde de la imagen.         |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es infinito para todas las entradas, excepto una imagen de entrada de tamaño 0. Si el alto o el ancho de una imagen de entrada es 0, el tamaño de salida es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

