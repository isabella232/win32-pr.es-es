---
description: Proporciona una interfaz de devolución de llamada para que la aplicación reciba un objeto de habilitador de contenido de la sesión de ruta de acceso multimedia protegida (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: MF_SESSION_CONTENT_PROTECTION_MANAGER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 753bd3e78be4d4996477cb597170c7a3396ae819766d3f4af9ac867055dd2dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691595"
---
# <a name="mf_session_content_protection_manager-attribute"></a>Atributo MF \_ SESSION \_ CONTENT PROTECTION \_ \_ MANAGER

Proporciona una interfaz de devolución de llamada para que la aplicación reciba un objeto de habilitador de contenido de la sesión de ruta de acceso multimedia protegida (PMP).

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Comentarios

El valor de este atributo es un puntero a la interfaz [**DEIContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de la aplicación.

Establezca este atributo en la sesión PMP mediante el *parámetro pConfiguration* de la [**función MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)

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

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos de sesión multimedia](media-session-attributes.md)
</dt> <dt>

[Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




