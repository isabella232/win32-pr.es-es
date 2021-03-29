---
title: Efecto de compensación de PPP
description: Use el efecto de compensación de PPP para ajustar automáticamente un mapa de bits de entrada para que coincida con el PPP del contexto. Esto resulta útil en situaciones en las que un mapa de bits se crea o se carga en un PPP diferente al de la pantalla.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905669"
---
# <a name="dpi-compensation-effect"></a>Efecto de compensación de PPP

Use el efecto de compensación de PPP para ajustar automáticamente un mapa de bits de entrada para que coincida con el PPP del contexto. Esto resulta útil en situaciones en las que un mapa de bits se crea o se carga en un PPP diferente al de la pantalla.

El CLSID para este efecto es CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                       | Descripción                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> \_Modo de \_ \_ interpolación de \_ propiedades de D2D1 DPICOMPENSATION<br/> | El modo de interpolación que el efecto usa para escalar la imagen.<br/> El tipo es D2D1 \_ DPICOMPENSATION \_ modo de interpolación \_ .<br/> El valor predeterminado es D2D1 \_ DPICOMPENSATION \_ modo de interpolación \_ \_ lineal.<br/>                  |
| BorderMode<br/> D2D1 \_ DPICOMPENSATION \_ \_ modo de borde \_ de la Prop<br/>               | El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea [modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información. <br/> El tipo es D2D1 \_ Border \_ mode.<br/> El valor predeterminado es D2D1 \_ Border \_ Mode \_ .<br/> |
| InputDpi<br/> \_PPP de \_ \_ entrada \_ de D2D1 DPICOMPENSATION<br/>                   | PPP de la imagen de entrada.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 96.0 f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                       | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de interpolación DPICOMPENSATION \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ \_ modo de interpolación DPICOMPENSATION \_ \_ lineal                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| D2D1 \_ \_ modo de interpolación DPICOMPENSATION \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ DPICOMPENSATION \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| D2D1 \_ \_ modo de interpolación DPICOMPENSATION \_ \_ anisotrópico           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ DPICOMPENSATION \_ modo de interpolación de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 DPICOMPENSTION \_ \_ lineal.

 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | Los píxeles que están fuera de los límites de entrada se generan mediante el [efecto de borde del reflejo](border.md). <br/> |
| D2D1 \_ del \_ modo de borde \_ | Los píxeles que están fuera de los límites de entrada son negros transparentes.<br/>                                    |



 

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

 

