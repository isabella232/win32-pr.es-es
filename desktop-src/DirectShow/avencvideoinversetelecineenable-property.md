---
description: Especifica si el codificador realiza televisa inversa.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propiedad AVEncVideoInverseTeledivable (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83eabd445b6070cfc77aeb4499da4268cafc11560d2c8db106b7d5dbecf9eb46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342165"
---
# <a name="avencvideoinversetelecineenable-property"></a>PROPIEDAD AVEncVideoInverseTeledivable

Especifica si el codificador realiza televisa inversa.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoInverseTelederoEnable**

## <a name="remarks"></a>Comentarios

Si el valor es **VARIANT \_ TRUE,** el codificador realiza una televersión inversa. Si no se requiere televisa inversa, establezca esta propiedad en **VARIANT \_ FALSE.** Para realizar televisa inversa fuera del codificador, establezca esta propiedad en **VARIANT \_ FALSE** y establezca la propiedad [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) en eAVEncVideoOutputScan \_ SameAsInput.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




