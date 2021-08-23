---
description: Especifica para una topología de transcodificación si el cargador de topologías cargará transformaciones basadas en hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e8715c135e074956af2280b8474172e94e69e1cca20cd01b020fc6dc79076c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663845"
---
# <a name="mf_transcode_topologymode-attribute"></a>Atributo \_ MF TRANSCODE \_ TOPOLOGYMODE

Especifica para una topología de transcodificación si el cargador de topologías cargará transformaciones basadas en hardware.

El modo de topología especifica si se pueden usar transformaciones de hardware (como códecs de hardware) en la topología de transcodificación. La aplicación puede almacenar este atributo en un perfil de transcodificación llamando a [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo de datos

**[**MF \_ MARCAS TRANSCODE \_ TOPOLOGYMODE \_ almacenadas**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** **como UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Debe tener uno de los siguientes valores.



| Valor                                              | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_SE PERMITE EL HARDWARE MF TRANSCODE \_ TOPOLOGYMODE \_ \_** | El cargador de topologías cargará las MTA basadas en hardware, como los descodificadores de hardware, cuando estén disponibles.<br/> El cargador de topologías vuelve automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no se conecta por algún motivo.<br/> |
| **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**    | El cargador de topologías solo cargará las MTA de software, incluidos los descodificadores de software.                                                                                                                                                                                                    |



 

El valor predeterminado es **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**.

Si el cargador de topologías inserta un MFT de hardware en la topología, establece el atributo atributo de dirección URL de HARDWARE de [MFT \_ ENUM \_ \_ \_ ](mft-enum-hardware-url-attribute.md) en el nodo de topología. Para comprobar si existe un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




