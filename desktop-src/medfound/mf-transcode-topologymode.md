---
description: Especifica para una topología de transcodificación si el cargador de topología va a cargar transformaciones basadas en hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908251"
---
# <a name="mf_transcode_topologymode-attribute"></a>\_Atributo TOPOLOGYMODE de TRANSCODE MF \_

Especifica para una topología de transcodificación si el cargador de topología va a cargar transformaciones basadas en hardware.

El modo de topología especifica si se pueden usar transformaciones de hardware (como códecs de hardware) en la topología de transcodificación. La aplicación puede almacenar este atributo en un perfil de transcodificación llamando a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo de datos

**[**MF \_ Transcodificar las \_ \_ marcas TOPOLOGYMODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** almacenadas como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Debe tener uno de los valores siguientes.



| Value                                              | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **se \_ permite el \_ hardware TOPOLOGYMODE de TRANScodificación MF \_ \_** | El cargador de topología cargará los MFTs basados en hardware, como los descodificadores de hardware, si están disponibles.<br/> El cargador de topología recurre automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no puede conectarse por algún motivo.<br/> |
| **MF \_ Transcode \_ TOPOLOGYMODE \_ \_ solo software**    | El cargador de topología solo cargará software MFTs, incluidos los descodificadores de software.                                                                                                                                                                                                    |



 

El valor predeterminado es **MF \_ Transcode \_ TOPOLOGYMODE \_ \_ solo software**.

Si el cargador de topología inserta un MFT de hardware en la topología, establece el atributo de [ \_ atributo de \_ \_ dirección URL \_ de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en el nodo de la topología. Para comprobar si existe un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.

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

[API de transcodificación](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




