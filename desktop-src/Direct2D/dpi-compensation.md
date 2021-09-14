---
title: Efecto de compensación de PPP
description: Use el efecto de compensación de PPP para ajustar automáticamente un mapa de bits de entrada para que coincida con el VALOR PPP del contexto. Esto es útil para situaciones en las que se crea o se carga un mapa de bits con un PPP diferente al de la pantalla.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163306"
---
# <a name="dpi-compensation-effect"></a>Efecto de compensación de PPP

Use el efecto de compensación de PPP para ajustar automáticamente un mapa de bits de entrada para que coincida con el VALOR PPP del contexto. Esto es útil para situaciones en las que se crea o se carga un mapa de bits con un PPP diferente al de la pantalla.

El CLSID para este efecto es CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                       | Descripción                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> D2D1 \_ PPPCOMPENSATION \_ PROP \_ INTERPOLATION \_ MODE<br/> | Modo de interpolación que usa el efecto para escalar la imagen.<br/> El tipo es D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE.<br/> El valor predeterminado es D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE LINEAR \_ .<br/>                  |
| BorderMode<br/> D2D1 \_ PPPCOMPENSATION \_ PROP BORDER \_ \_ MODE<br/>               | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte [Modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información. <br/> El tipo es D2D1 \_ BORDER \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ MODE \_ SOFT.<br/> |
| InputDpi<br/> PPP DE D2D1 \_ PPPCOMPENSATION \_ PROP \_ INPUT \_ PPP<br/>                   | Ppp de la imagen de entrada.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 96,0f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                       | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE NEAREST \_ \_ NEIGHBOR     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE MULTI \_ \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ PPPCOMPENSATION \_ INTERPOLATION \_ MODE HIGH \_ \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ PPPCOMPENSTION \_ INTERPOLATION MODE LINEAR(LINEAL MODO DE INTERPOLACIÓN DE PPPCOMPENSTION \_ \_ D2D1).

 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto del borde reflejado genera píxeles fuera de los límites [de entrada.](border.md) <br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | Los píxeles fuera de los límites de entrada son de color negro transparente.<br/>                                    |



 

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

 

