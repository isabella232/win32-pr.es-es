---
description: Contiene el CLSID de un cargador de topología para la sesión multimedia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716953"
---
# <a name="mf_session_topoloader-attribute"></a>\_Atributo TOPOLOADER de sesión MF \_

Contiene el CLSID de un cargador de topología para la sesión multimedia.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Puede usar este atributo para proporcionar un cargador de topología personalizado para la sesión multimedia.

Establezca este atributo mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Si se establece este atributo, la sesión multimedia llama a **CoCreateInstance** con el CLSID especificado al crear el cargador de topología. El objeto creado por este CLSID debe exponer la interfaz [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Si no se establece este atributo, la sesión multimedia crea el cargador de topología predeterminado proporcionado en Media Foundation.

Un cargador de topología debe admitir apartamentos multiproceso. Debe registrar el cargador de topología como ThreadingModel = "both". Además, si usa el cargador de topología dentro de la ruta de acceso a medios protegidos (PMP), el cargador de topología debe ser un componente de confianza. Para obtener más información, vea [ruta de acceso a medios protegidos](protected-media-path.md).

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

[**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Atributos de la sesión multimedia](media-session-attributes.md)
</dt> <dt>

[Cargadores de topología personalizados](custom-topology-loaders.md)
</dt> </dl>

 

 




