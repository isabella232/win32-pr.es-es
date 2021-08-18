---
description: Especifica el número máximo de fotogramas que almacenará en búfer el origen de captura de vídeo.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba50ad5489d08ba0fc986d56bef8d57c547fa0146a3bbb58290bca43009cc5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973824"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>Atributo MF \_ DEVSOURCE \_ \_ SOURCE TYPE \_ \_ VIDCAP MAX \_ \_ BUFFERS

Especifica el número máximo de fotogramas que almacenará en búfer el origen de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

De forma predeterminada, el origen de captura de vídeo almacena en búfer un máximo de un fotograma a la vez. Puede aumentar el límite de búfer estableciendo este atributo.

La manera correcta de establecer este atributo depende de la función utilizada para crear el origen multimedia:

-   [**MFCreateDeviceSource:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)establezca el atributo a través del *parámetro pAttributes* de la función.
-   [**MFCreateDeviceSourceActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)establezca el atributo a través del *parámetro pAttributes* de la función.
-   [**MFEnumDeviceSources:**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)establezca el atributo en el puntero [**DE LAACTIVATE devuelto**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) por la función. Establezca el atributo antes de llamar [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

El atributo solo se aplica a los dispositivos de captura de vídeo.

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

 

 




