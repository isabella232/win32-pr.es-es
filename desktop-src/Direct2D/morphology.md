---
title: Efecto de morfología
description: Use el efecto de morfología para estrechar o aumentar el grosor de los límites de una imagen.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- efectos de morfología
- efecto de desactivación
- efecto de mermas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150635"
---
# <a name="morphology-effect"></a>Efecto de morfología

Use el efecto de morfología para estrechar o aumentar el grosor de los límites de una imagen. Este efecto crea un kernel que es 2 veces los valores de ancho y alto que especifique. Este efecto centra el kernel en el píxel que está calculando y devuelve el valor máximo en el kernel (si dilating) o el valor mínimo en el kernel (si Eroding).

El CLSID para este efecto es CLSID \_ D2D1Morphology.

## <a name="example-images"></a>Imágenes de ejemplo

En este ejemplo se muestra el resultado del efecto al utilizar el modo de.



| Antes                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
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



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                          | Tipo y valor predeterminado                                                     | Descripción                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> D2D1 \_ \_ modo de propuesta de morfología \_<br/>     | \_Modo de morfología de D2D1 \_<br/> D2D1 \_ el \_ modo de morfología \_<br/> | Modo de morfología. Los modos disponibles son (Flatten) y Dilate (espesor).<br/> Vea [modos de morfología](#morphology-modes) para obtener más información.<br/> |
| Ancho<br/> Ancho de la D2D1 \_ morfología \_ \_<br/>   | UINT<br/> 1<br/>                                               | Tamaño del kernel en la dirección X. Las unidades están en DIP. Los valores deben estar entre 1 y 100, ambos inclusive.                                                         |
| Alto<br/> Alto de la D2D1 \_ morfología \_ \_<br/> | UINT<br/> 1<br/>                                               | Tamaño del kernel en la dirección Y. Las unidades están en DIP. Los valores deben estar entre 1 y 100, ambos inclusive.                                                         |



 

## <a name="morphology-modes"></a>Modos de morfología



| Nombre                           | Descripción                                                    |
|--------------------------------|----------------------------------------------------------------|
| D2D1 \_ el \_ modo de morfología \_  | Se usa el valor máximo de cada canal RGB en el kernel. |
| Desreferenciado del modo de \_ morfología D2D1 \_ \_ | Se usa el valor mínimo de cada canal RGB en el kernel. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

En el modo de tiempo de ejecución, el tamaño del mapa de bits de salida crece: 

| Requisito | Value |
|--------------------------|-----------------------------------------|
| Crecimiento de mapa de bits de salida X = | INT (FLOAT (ancho) \* ((PPP del usuario)/96))  |
| Crecimiento de mapa de bits de salida Y = | INT (FLOAT (alto) \* ((PPP del usuario)/96)) |



 

En el modo de disminución, se reduce el tamaño del mapa de bits de salida:

| Requisito | Value |
|--------------------------|------------------------------------------|
| Crecimiento de mapa de bits de salida X = | INT (FLOAT (-width) \* ((PPP de usuario)/96))  |
| Crecimiento de mapa de bits de salida Y = | INT (FLOAT (-height) \* ((PPP de usuario)/96)) |



 

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

 

