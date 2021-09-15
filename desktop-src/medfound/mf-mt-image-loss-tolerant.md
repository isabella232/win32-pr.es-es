---
description: Especifica si un flujo de imagen de ASF es un tipo JPEG degradable.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468684"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>Atributo MF \_ MT \_ IMAGE \_ LOSS \_ TOLERANT

Especifica si un flujo de imagen de ASF es un tipo JPEG degradable.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Este atributo se aplica al tipo de medio para los flujos de imágenes en ASF. Si el valor es **TRUE,** la secuencia es un tipo de imagen JPEG degradable. De lo contrario, la secuencia es un tipo de imagen JFIF. Para obtener más información sobre estos tipos de flujo, consulte la especificación de ASF.

Además del atributo MF MT IMAGE LOSS TOLERANT, el tipo de medio para un flujo de \_ \_ imagen de \_ \_ ASF contiene los siguientes atributos:



| Atributo                                                 | Descripción                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md) | Contiene el valor **MFMediaType \_ Image**. |
| [**TAMAÑO \_ DEL MARCO DE MT \_ \_ DE MF**](mf-mt-frame-size-attribute.md) | Proporciona el tamaño de la imagen en píxeles.            |



 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




