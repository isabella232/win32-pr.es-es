---
title: Efecto premultiplicado
description: Use este efecto para convertir una imagen de alfa sin multiplicar a alfa premultiplicado.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- efecto premultiplicado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af158ab8f885c51d2dce15d5bfbc5c24f34f6a980ebc8e8f4631617d31a2a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075029"
---
# <a name="premultiply-effect"></a>Efecto premultiplicado

Use este efecto para convertir una imagen de alfa sin multiplicar a alfa premultiplicado. El efecto reemplaza cada píxel de entrada `P = {R, G, B, A}` por `P' = {R*A, G*A, B*A, A}` en la salida.

Este efecto no tiene propiedades.

El CLSID para este efecto es CLSID \_ D2D1Premultiply.

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
