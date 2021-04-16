---
description: Especifica el CLSID de un complemento de procesamiento posterior para un dispositivo de captura de vídeo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696602"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>\_ \_ \_ Atributo CLSID del complemento de extensión MF DEVICESTREAM \_

Especifica el CLSID de un complemento de procesamiento posterior para un dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Un complemento de procesamiento posterior es un MFT que procesa la imagen de vídeo una vez capturada. El fabricante del hardware puede incluir un complemento de procesamiento posterior como parte del paquete de instalación. Si es así, el origen de captura de vídeo establece el \_ \_ \_ atributo CLSID del complemento de extensión MF DEVICESTREAM \_ en el CLSID del complemento.

Para obtener este atributo, haga lo siguiente:

1.  Consulte el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.
3.  Llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) para obtener el atributo.

Para crear el complemento, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
