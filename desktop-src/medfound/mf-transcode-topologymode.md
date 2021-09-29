---
description: Especifica para una topología de transcodificación si el cargador de topologías cargará transformaciones basadas en hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360451"
---
# <a name="mf_transcode_topologymode-attribute"></a>Atributo MF \_ TRANSCODE \_ TOPOLOGYMODE

Especifica para una topología de transcodificación si el cargador de topologías cargará transformaciones basadas en hardware.

El modo de topología especifica si se pueden usar transformaciones de hardware (como códecs de hardware) en la topología de transcodificación. La aplicación puede almacenar este atributo en un perfil de transcodificación llamando a [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo de datos

**[**MF \_ MARCAS TRANSCODE \_ TOPOLOGYMODE \_ almacenadas**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** **como UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Debe tener uno de los siguientes valores.



| Value                                              | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ HARDWARE \_ ALLOWED** | El cargador de topologías cargará los MFT basados en hardware, como los descodificadores de hardware, cuando estén disponibles.<br/> El cargador de topologías vuelve automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no se puede conectar por algún motivo.<br/> |
| **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**    | El cargador de topologías cargará solo las MTA de software, incluidos los descodificadores de software.                                                                                                                                                                                                    |



 

El valor predeterminado es **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**.

Si el cargador de topologías inserta un MFT de hardware en la topología, establece el atributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) en el nodo de topología. Para comprobar si hay un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




