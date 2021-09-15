---
description: Especifica si el receptor sample-grabber usa el reloj de presentación para programar muestras.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579865"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>Atributo \_ MF SAMPLEGRABBERSINK \_ IGNORE \_ CLOCK

Especifica si el receptor sample-grabber usa el reloj de presentación para programar muestras.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Puede establecer este atributo en el objeto de activación creado por la [**función MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Establezca el atributo antes de llamar al [**método IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.

De forma predeterminada, cuando el receptor sample-grabber recibe una muestra, espera hasta el tiempo de presentación del ejemplo para invocar la devolución de llamada de la aplicación. Si el atributo MF SAMPLEGRABBERSINK IGNORE CLOCK es distinto de cero, el receptor \_ \_ sample-grabber omite el reloj de presentación e invoca la devolución de llamada en cuanto recibe cada \_ muestra.

Uso recomendado:

-   Si desea procesar ejemplos lo antes posible, establezca este atributo en **TRUE.**
-   Si desea que las llamadas al método de devolución de llamada se sincronicen con el reloj, no establezca este atributo o esta establezca en **FALSE.** Puede obtener muestras ligeramente antes del reloj, mientras permanece sincronizado, estableciendo el atributo [**MF \_ SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET.**](mf-samplegrabbersink-sample-time-offset-attribute.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




