---
description: Especifica si el codificador realiza telecine inversa.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propiedad AVEncVideoInverseTelecineEnable (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152494"
---
# <a name="avencvideoinversetelecineenable-property"></a>Propiedad AVEncVideoInverseTelecineEnable

Especifica si el codificador realiza telecine inversa.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoInverseTelecineEnable**

## <a name="remarks"></a>Observaciones

Si el valor es **Variant \_ true**, el codificador realiza telecine inversa. Si no se requiere telecine inversa, establezca esta propiedad en **Variant \_ false**. Para realizar telecine inversa fuera del codificador, establezca esta propiedad en **Variant \_ false** y establezca la propiedad [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) en eAVEncVideoOutputScan \_ SameAsInput.

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

 

 




