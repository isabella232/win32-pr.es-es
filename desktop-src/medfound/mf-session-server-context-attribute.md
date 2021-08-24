---
description: Permite que dos instancias de la sesión de medios compartan el mismo proceso de ruta de acceso multimedia protegida (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: MF_SESSION_SERVER_CONTEXT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9674a2e25a7cdfd0a88ebcc43c18d6fd636bf22116f76a24255b55f857a677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102341"
---
# <a name="mf_session_server_context-attribute"></a>Atributo \_ CONTEXT DE MF SESSION \_ SERVER \_

Permite que dos instancias de la sesión de medios compartan el mismo proceso de ruta de acceso multimedia protegida (PMP).

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Comentarios

Use este atributo si desea crear la sesión multimedia de PMP en un proceso de PMP existente. El valor del atributo es un puntero a la [**interfaz IMFPMPServer.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos de sesión multimedia](media-session-attributes.md)
</dt> </dl>

 

 




