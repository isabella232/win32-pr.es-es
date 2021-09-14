---
description: Especifica el número de campos que se omitirán durante la codificación.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Propiedad AVEncVideoNoOfFieldsToSkip (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708ef409fb907520d6a582599da2050a1353636c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161750"
---
# <a name="avencvideonooffieldstoskip-property"></a>Propiedad AVEncVideoNoOfFieldsToSkip

Especifica el número de campos que se omitirán durante la codificación.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Observaciones

En el caso del vídeo progresiva, establezca esta propiedad en el doble del número de fotogramas que se omitirán.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




