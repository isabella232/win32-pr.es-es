---
title: Efecto premultiplicado
description: Use este efecto para convertir una imagen de alfa sin multiplicar a alfa premultiplicado.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- efecto premultiplicado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162638"
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
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
