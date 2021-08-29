---
description: Contiene el CLSID de un administrador de calidad para la sesión multimedia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: MF_SESSION_QUALITY_MANAGER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049ecde194f7cccf97460ac99c566815d43b222132f72b70a0874719fc663c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691585"
---
# <a name="mf_session_quality_manager-attribute"></a>Atributo \_ MF SESSION QUALITY \_ \_ MANAGER

Contiene el CLSID de un administrador de calidad para la sesión multimedia.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Puede usar este atributo para proporcionar un administrador de calidad personalizado para la sesión multimedia.

Establezca este atributo mediante el *parámetro pConfiguration* de la [**función MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) [**o MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)

Si se establece este atributo, la sesión multimedia llama a **CoCreateInstance** con el CLSID especificado para crear el administrador de calidad. El objeto creado por este CLSID debe exponer la [**interfaz IMFQualityManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)

Si no se establece este atributo, la sesión multimedia crea el administrador de calidad predeterminado proporcionado en Media Foundation.

Si desea ejecutar la sesión multimedia sin ningún administrador de calidad, establezca este atributo en **GUID \_ NULL.**

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Atributos de sesión multimedia](media-session-attributes.md)
</dt> </dl>

 

 




