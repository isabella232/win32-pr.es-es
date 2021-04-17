---
title: Efecto de borde
description: Use el efecto de borde para extender una imagen de los bordes.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- efecto de borde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104547243"
---
# <a name="border-effect"></a>Efecto de borde

Use el efecto de borde para extender una imagen de los bordes. Puede usar este efecto para repetir los píxeles desde los bordes de la imagen, ajustar los píxeles desde el extremo opuesto de la imagen o reflejar los píxeles en el borde del mapa de bits para extender la región del mapa de bits.

El CLSID para este efecto es CLSID \_ D2D1Border.

## <a name="example-images"></a>Imágenes de ejemplo

En los ejemplos siguientes se muestra el resultado del efecto de borde con cada modo. El tamaño de salida es infinito, pero estas imágenes de ejemplo se recortan dos veces el tamaño.

### <a name="mirror"></a>Reflejo



| Antes                                                    |
|-----------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto.](images/border-before.jpg) |
| Después                                                     |
| ![Captura de pantalla que muestra la imagen después de la transformación.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Antes                                                        |
|---------------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto de una abrazadera.](images/border-before.jpg)     |
| Después                                                         |
| ![Captura de pantalla que muestra la imagen después de la transformación de una abrazadera.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Encapsulado



| Antes                                                       |
|--------------------------------------------------------------|
| ![Captura de pantalla que muestra la imagen antes del efecto para un ajuste.](images/border-before.jpg)    |
| Después                                                        |
| ![Captura de pantalla que muestra la imagen después de la transformación de un ajuste.](images/10-border-wrap.png) |



 


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



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                  | Descripción                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modo de borde X<br/> D2D1 \_ Border \_ props \_ modo de borde \_ \_ X<br/> | Modo de borde en la dirección X del efecto. Puede establecerlo en Clamp, Wrap o Mirror. Vea [modos perimetrales](#edge-modes) para obtener más información.<br/> El tipo es el modo de borde de borde de D2D1 \_ \_ \_ .<br/> El valor predeterminado es la abrazadera del modo de borde de \_ borde D2D1 \_ \_ \_ .<br/> |
| Modo de borde Y<br/> Modo de borde de propiedades de borde de D2D1 \_ \_ \_ \_ \_ Y<br/> | Modo de borde en la dirección Y del efecto. Puede establecerlo en Clamp, Wrap o Mirror. Vea [modos perimetrales](#edge-modes) para obtener más información.<br/> El tipo es el modo de borde de borde de D2D1 \_ \_ \_ .<br/> El valor predeterminado es la abrazadera del modo de borde de \_ borde D2D1 \_ \_ \_ .<br/> |



 

## <a name="edge-modes"></a>Modos perimetrales



| Enumeración de índice y nombre para mostrar                            | Descripción                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> \_Abrazadera del \_ \_ modo \_ de borde de borde de D2D1<br/>   | Repite los píxeles de los bordes de la imagen.      |
| Encapsulado<br/> \_Ajuste del \_ \_ modo \_ de borde de borde de D2D1<br/>     | Usa píxeles desde el borde final opuesto de la imagen. |
| Reflejo<br/> \_Reflejo del \_ \_ modo \_ de borde de D2D1 Border<br/> | Refleja los píxeles sobre el borde de la imagen.         |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es infinito para todas las entradas, excepto una imagen de entrada de tamaño 0. Si el alto o el ancho de una imagen de entrada es 0, el tamaño de salida es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

