---
description: Especifica que el origen de medios se creará en un proceso remoto.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: MF_SESSION_REMOTE_SOURCE_MODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277831"
---
# <a name="mf_session_remote_source_mode-attribute"></a>\_Atributo de \_ \_ modo de origen remoto de sesión MF \_

Especifica que el origen de medios se creará en un proceso remoto.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Puede establecer este atributo en la sesión de la ruta de acceso a medios protegidos (PMP) mediante el parámetro *pConfiguration* de la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Atributos de la sesión multimedia](media-session-attributes.md)
</dt> <dt>

[Sesión de medios de PMP](pmp-media-session.md)
</dt> </dl>

 

 




