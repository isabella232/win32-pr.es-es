---
description: Especifica si un descodificador de AAC usa ecuaciones estándar mpeg-2/MPEG-4 de reducción estéreo, o bien una reducción no estándar.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propiedad AVDecAACDownmixMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3fde61acdd5d29574f316e269d5b04a0a94649827777504fe31c33bbf79bd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641285"
---
# <a name="avdecaacdownmixmode-property"></a>Propiedad AVDecAACDownmixMode

Especifica si un descodificador de AAC usa ecuaciones estándar mpeg-2/MPEG-4 de reducción estéreo, o bien una reducción no estándar.

Un ejemplo de una mezcla anterior no estándar es la definida por el documento STD-B21 de ARIB, versión 4.4.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDecAACDownmixMode.**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

