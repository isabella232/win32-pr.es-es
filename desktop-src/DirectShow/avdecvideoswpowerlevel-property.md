---
description: Especifica el nivel de ahorro de energía de un descodificador de vídeo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propiedad AVDecVideoSWPowerLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666131"
---
# <a name="avdecvideoswpowerlevel-property"></a>Propiedad AVDecVideoSWPowerLevel

Especifica el nivel de ahorro de energía de un descodificador de vídeo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valor de propiedad

El intervalo de valores posibles es \[ 0.. 100 \] , ambos inclusive, con el significado siguiente.



| Value | Descripción                 |
|-------|-----------------------------|
| 0     | Optimizar para la duración de la batería.  |
| 100   | Optimice la calidad del vídeo. |



 

La enumeración [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) define algunas constantes específicas dentro de este intervalo.

## <a name="remarks"></a>Observaciones

Puede establecer esta propiedad durante la reproducción para cambiar el nivel de ahorro de energía.

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

 

 




