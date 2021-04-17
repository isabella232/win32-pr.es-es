---
description: Especifica si el receptor de captura de muestra usa el reloj de presentación para programar ejemplos.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716346"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>MF \_ SAMPLEGRABBERSINK \_ omitir \_ atributo de reloj

Especifica si el receptor de captura de muestra usa el reloj de presentación para programar ejemplos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Puede establecer este atributo en el objeto de activación creado por la función [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Establezca el atributo antes de llamar al método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.

De forma predeterminada, cuando el receptor del captador de muestra recibe un ejemplo, espera hasta que el tiempo de presentación del ejemplo invoque la devolución de llamada de la aplicación. Si el \_ \_ atributo de reloj MF SAMPLEGRABBERSINK omitir \_ es distinto de cero, el receptor de captura de muestras omite el reloj de la presentación e invoca la devolución de llamada en cuanto recibe cada ejemplo.

Uso recomendado:

-   Si desea procesar los ejemplos lo más rápido posible, establezca este atributo en **true**.
-   Si desea que las llamadas al método de devolución de llamada se sincronicen con el reloj, no establezca este atributo o establézcalo en **false**. Puede obtener ejemplos ligeramente por encima del reloj, mientras sigue sincronizando, estableciendo el atributo de [**desplazamiento de \_ \_ \_ tiempo \_ de ejemplo MF SAMPLEGRABBERSINK**](mf-samplegrabbersink-sample-time-offset-attribute.md) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




