---
description: Especifica el nivel de ahorro de energía de un descodificador de vídeo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propiedad AVDecVideoSWPowerLevel (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c362e066a16e333cda402704a720b5e1b0b8534f1b56536d32009e6fa29663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824225"
---
# <a name="avdecvideoswpowerlevel-property"></a>Propiedad AVDecVideoSWPowerLevel

Especifica el nivel de ahorro de energía de un descodificador de vídeo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valor de propiedad

El intervalo de valores posibles \[ es 0..100, \] ambos incluidos, con el significado siguiente.



| Valor | Descripción                 |
|-------|-----------------------------|
| 0     | Optimice la duración de la batería.  |
| 100   | Optimización de la calidad del vídeo. |



 

La [**enumeración eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) define algunas constantes específicas dentro de este intervalo.

## <a name="remarks"></a>Comentarios

Puede establecer esta propiedad durante la reproducción para cambiar el nivel de ahorro de energía.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




