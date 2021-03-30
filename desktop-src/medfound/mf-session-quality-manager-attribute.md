---
description: Contiene el CLSID de un administrador de calidad para la sesión multimedia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: MF_SESSION_QUALITY_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360930"
---
# <a name="mf_session_quality_manager-attribute"></a>\_Atributo de \_ Administrador de calidad de sesión MF \_

Contiene el CLSID de un administrador de calidad para la sesión multimedia.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Puede usar este atributo para proporcionar un administrador de calidad personalizado para la sesión multimedia.

Establezca este atributo mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Si se establece este atributo, la sesión multimedia llama a **CoCreateInstance** con el CLSID especificado para crear el administrador de calidad. El objeto creado por este CLSID debe exponer la interfaz [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .

Si no se establece este atributo, la sesión multimedia crea el administrador de calidad predeterminado proporcionado en Media Foundation.

Si desea ejecutar la sesión de medios sin administrador de calidad, establezca este atributo en **GUID \_ null**.

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
</dt> </dl>

 

 




