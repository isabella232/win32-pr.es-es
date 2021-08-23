---
description: Contiene el vínculo simbólico para un controlador de captura de vídeo.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd3b69899eb9df1973cb13611a822139ffda0e744c84137ff9d6094ed4a962d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104951"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP SYMBOLIC \_ \_ LINK

Contiene el vínculo simbólico para un controlador de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**Wchar\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentarios

Use este atributo como entrada para la [**función MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)

Además, este atributo se establece en los objetos de activación devueltos por las funciones siguientes:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

El vínculo simbólico debe considerarse una cadena opaca. El nombre para mostrar legible para un dispositivo se encuentra en el atributo [MF \_ DEVSOURCE \_ ATTRIBUTE FRIENDLY \_ \_ NAME.](mf-devsource-attribute-friendly-name.md)

El atributo MF DEVSOURCE ATTRIBUTE SOURCE TYPE VIDCAP SYMBOLIC LINK se puede pasar como el valor del argumento DevicePath de la \_ \_ función \_ \_ \_ \_ \_ [**SetupDiOpenDeviceInterface.**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
