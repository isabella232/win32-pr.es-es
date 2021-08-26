---
description: Contiene el CLSID de un cargador de topologías para la sesión multimedia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9568193bbdbd46485015b6e5975db26fca2b552b23b7c227576e4e6544d69af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955135"
---
# <a name="mf_session_topoloader-attribute"></a>Atributo \_ MF SESSION \_ TOPOLOADER

Contiene el CLSID de un cargador de topologías para la sesión multimedia.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Puede usar este atributo para proporcionar un cargador de topología personalizado para la sesión multimedia.

Establezca este atributo mediante el *parámetro pConfiguration* de la [**función MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**la función MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)

Si se establece este atributo, la sesión multimedia llama a **CoCreateInstance** con el CLSID especificado cuando crea el cargador de topologías. El objeto creado por este CLSID debe exponer la [**interfaz DETOPOLoader.**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)

Si no se establece este atributo, la sesión multimedia crea el cargador de topología predeterminado proporcionado en Media Foundation.

Un cargador de topologías debe admitir departamentos multiproceso. Debe registrar el cargador de topologías como ThreadingModel="Both". Además, si usa el cargador de topologías dentro de la ruta de acceso de medios protegidos (PMP), el cargador de topologías debe ser un componente de confianza. Para obtener más información, vea [Ruta de acceso multimedia protegida.](protected-media-path.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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
</dt> <dt>

[Cargadores de topología personalizados](custom-topology-loaders.md)
</dt> </dl>

 

 




