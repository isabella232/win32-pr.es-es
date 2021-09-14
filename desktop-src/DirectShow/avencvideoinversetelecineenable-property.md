---
description: Especifica si el codificador realiza televisa inversa.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propiedad AVEncVideoInverseTeledivable (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161757"
---
# <a name="avencvideoinversetelecineenable-property"></a>PROPIEDAD AVEncVideoInverseTeledivable

Especifica si el codificador realiza televisa inversa.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoInverseTelederoEnable**

## <a name="remarks"></a>Observaciones

Si el valor es **VARIANT \_ TRUE,** el codificador realiza una televersión inversa. Si no se requiere televisa inversa, establezca esta propiedad en **VARIANT \_ FALSE.** Para realizar televisa inversa fuera del codificador, establezca esta propiedad en **VARIANT \_ FALSE** y establezca la propiedad [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) en eAVEncVideoOutputScan \_ SameAsInput.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




