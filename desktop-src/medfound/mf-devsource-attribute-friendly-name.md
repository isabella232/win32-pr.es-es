---
description: Especifica el nombre para mostrar de un dispositivo.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90e019b37b251ad8ec00efbd3bd0395659b96c6dd2e3a1cad247ea17ace3ece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973834"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE \_ FRIENDLY \_ NAME

Especifica el nombre para mostrar de un dispositivo. El *nombre para mostrar* es una cadena legible, adecuada para mostrarse en una interfaz de usuario.

## <a name="data-type"></a>Tipo de datos

**Wchar\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentarios

Este atributo se establece en los objetos de activación devueltos por las siguientes funciones:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




