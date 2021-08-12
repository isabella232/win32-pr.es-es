---
title: Efecto no multimultiplicación
description: Use este efecto para convertir una imagen de alfa premultiplicado a alfa sin multiplicar.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- efecto no multimultiplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152803956b9839b881404be013c521dc0f5bfc764b2f07a8462275b523ba762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664883"
---
# <a name="unpremultiply-effect"></a>Efecto no multimultiplicación

Use este efecto para convertir una imagen de alfa premultiplicado a alfa sin multiplicar. El efecto reemplaza cada píxel de entrada `P = {R, G, B, A}` por `P' = {R/A, G/A, B/A, A}` en la salida.

Este efecto no tiene propiedades.

El CLSID para este efecto es CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
