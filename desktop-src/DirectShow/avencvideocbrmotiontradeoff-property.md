---
description: Especifica el equilibrio entre las imágenes de movimiento y las imágenes fijas. Esta propiedad solo se aplica al modo de control de velocidad de bits constante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propiedad AVEncVideoCBRMotionTradeoff (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997957"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>Propiedad AVEncVideoCBRMotionTradeoff

Especifica el equilibrio entre las imágenes de movimiento y las imágenes fijas. Esta propiedad solo se aplica al modo de control de velocidad de bits constante (CBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoCBRMotionTradeoff**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el siguiente intervalo.



| Value | Descripción               |
|-------|---------------------------|
| 0     | Optimizar para imágenes fijas |
| 100   | Optimizar para el movimiento.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




