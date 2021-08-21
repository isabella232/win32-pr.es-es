---
description: Especifica si los metadatos se escriben en el archivo transcodificado.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: MF_TRANSCODE_SKIP_METADATA_TRANSFER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7874d7d8cc20bbf5222cd8fd2fa0ca938c0b597dbc42914ab809dad926968306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739427"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>Atributo SKIP \_ METADATA TRANSFER de TRANSCODE \_ \_ \_ DE MF

Especifica si los metadatos se escriben en el archivo transcodificado. Este atributo de contenedor se almacena en el perfil de transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Los valores posibles para el atributo SKIP METADATA TRANSFER de MF \_ TRANSCODE \_ se \_ \_ describen en la tabla siguiente.



| Value                                                                        | Significado                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Transfiere automáticamente los metadatos de nivel de archivo del archivo de origen al archivo transcodificado.<br/> |
| <dl> <dt>1</dt> </dl> | Los metadatos del archivo de origen no se escriben en el archivo transcodificado.<br/>                          |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




