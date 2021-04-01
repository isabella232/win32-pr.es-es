---
description: Especifica si los metadatos se escriben en el archivo transcodificado.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: MF_TRANSCODE_SKIP_METADATA_TRANSFER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275685"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>MF \_ Transcode \_ omitir \_ atributo de transferencia de metadatos \_

Especifica si los metadatos se escriben en el archivo transcodificado. Este atributo de contenedor se almacena en el perfil de transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

\_ \_ \_ \_ En la tabla siguiente se describen los posibles valores para el atributo de transferencia de metadatos del salto de transcodificación de MF.



| Value                                                                        | Significado                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Transfiere automáticamente los metadatos de nivel de archivo del archivo de código fuente al archivo transcodificado.<br/> |
| <dl> <dt>1</dt> </dl> | Los metadatos del archivo de origen no se escriben en el archivo transcodificado.<br/>                          |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

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

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




