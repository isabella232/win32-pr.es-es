---
title: Efecto de la morfología
description: Use el efecto de la morfología para delimitar o engrosar los límites de borde de una imagen.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- Efectos de la morfología
- efecto de la reenlaz
- Efecto de e ya no
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162685"
---
# <a name="morphology-effect"></a>Efecto de la morfología

Use el efecto de la morfología para delimitar o engrosar los límites de borde de una imagen. Este efecto crea un kernel que es 2 veces el valor de Width y Height que especifique. Este efecto centra el kernel en el píxel que está calculando y devuelve el valor máximo en el kernel (si se vuelve a calcular) o el valor mínimo en el kernel (si se está desasoyendo).

El CLSID para este efecto es CLSID \_ D2D1Morphology.

## <a name="example-images"></a>Imágenes de ejemplo

En este ejemplo se muestra la salida del efecto cuando se usa el modo etensión.



| Antes                                                     |
|------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg) |
| Después                                                      |
| ![la imagen después de la transformación.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                          | Tipo y valor predeterminado                                                     | Descripción                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> MODO PROP \_ DE MORPHOLOGY D2D1 \_ \_<br/>     | MODO \_ MORPHOLOGY D2D1 \_<br/> ETROP \_ DEL MODO MORPHOLOGY \_ \_ D2D1<br/> | Modo de morfología. Los modos disponibles son ellano (aplanado) y entrete (grueso).<br/> Para [más información, consulte](#morphology-modes) Modos de morfología.<br/> |
| Ancho<br/> D2D1 \_ MORPHOLOGY \_ PROP \_ WIDTH<br/>   | UINT<br/> 1<br/>                                               | Tamaño del kernel en la dirección X. Las unidades están en DIP. Los valores deben estar entre 1 y 100 inclusive.                                                         |
| Alto<br/> D2D1 \_ MORPHOLOGY \_ PROP \_ HEIGHT<br/> | UINT<br/> 1<br/>                                               | Tamaño del kernel en la dirección Y. Las unidades están en DIP. Los valores deben estar entre 1 y 100 inclusive.                                                         |



 

## <a name="morphology-modes"></a>Modos de morfología



| Nombre                           | Descripción                                                    |
|--------------------------------|----------------------------------------------------------------|
| ETROP \_ DEL MODO MORPHOLOGY \_ \_ D2D1  | Se usa el valor máximo de cada canal RGB del kernel. |
| MODO MORPHOLOGY DE D2D1: \_ \_ \_ ENTRETE | Se usa el valor mínimo de cada canal RGB del kernel. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

Para el modo DESEMITA, el tamaño del mapa de bits de salida aumenta: 

| Requisito | Value |
|--------------------------|-----------------------------------------|
| Output Bitmap Growth X = | INT(FLOAT(Width) \* ((User PPP) / 96))  |
| Crecimiento del mapa de bits de salida Y = | INT(FLOAT(Height) \* ((User PPP) / 96)) |



 

Para el modo ENTES, el tamaño del mapa de bits de salida se reduce:

| Requisito | Value |
|--------------------------|------------------------------------------|
| Output Bitmap Growth X = | INT(FLOAT(-Width) \* ((USER PPP) / 96))  |
| Crecimiento del mapa de bits de salida Y = | INT(FLOAT(-Height) \* ((User PPP) / 96)) |



 

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

 

