---
description: Especifica el CLSID de un complemento de procesamiento posterior para un dispositivo de captura de vídeo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a474d66bfaa079cfc7b5e483ad1f10b3c09e600437f841fc062db8f0ca611d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956705"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>Atributo \_ \_ \_ \_ CLSID del COMPLEMENTO DE EXTENSIÓN MF DEVICESTREAM

Especifica el CLSID de un complemento de procesamiento posterior para un dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Un complemento posterior al procesamiento es un MFT que procesa la imagen de vídeo después de capturarla. El proveedor de hardware puede incluir un complemento posterior al procesamiento como parte del paquete de instalación. Si es así, el origen de captura de vídeo establece el atributo CLSID del complemento MF DEVICESTREAM EXTENSION en el \_ \_ \_ \_ CLSID del complemento.

Para obtener este atributo, haga lo siguiente:

1.  Consulte el origen de medios para la [**interfaz IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
2.  Llame [**a IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.
3.  Llame [**a IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) para obtener el atributo.

Para crear el complemento, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
