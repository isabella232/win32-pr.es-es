---
description: Proporciona una interfaz de devolución de llamada para que la aplicación reciba un objeto de habilitador de contenido de la sesión de la ruta de acceso a medios protegidos (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: MF_SESSION_CONTENT_PROTECTION_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716491"
---
# <a name="mf_session_content_protection_manager-attribute"></a>\_Atributo de \_ Administrador de protección de contenido de sesión MF \_ \_

Proporciona una interfaz de devolución de llamada para que la aplicación reciba un objeto de habilitador de contenido de la sesión de la ruta de acceso a medios protegidos (PMP).

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [_ *IMFContentProtectionManager* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de la aplicación.

Establezca este atributo en la sesión de PMP mediante el parámetro *pConfiguration* de la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos de la sesión multimedia](media-session-attributes.md)
</dt> <dt>

[Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




