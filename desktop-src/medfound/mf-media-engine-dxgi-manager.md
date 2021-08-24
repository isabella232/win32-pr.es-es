---
description: Establece el Infraestructura de gráficos de DirectX de Microsoft (DXGI) Administrador de dispositivos en el motor multimedia.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: MF_MEDIA_ENGINE_DXGI_MANAGER atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c454041f83a58cdb5b3c1e340d63908386546090eb52811e0c876e5d8bed0bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723058"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>Atributo \_ \_ DXGI MANAGER de MF MEDIA ENGINE \_ \_

Establece el Infraestructura de gráficos de DirectX de Microsoft (DXGI) Administrador de dispositivos en el motor multimedia.

## <a name="data-type"></a>Tipo de datos

**IMFDXGIDeviceManager \* *_ almacenado como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentarios

El valor de este atributo es un puntero a la [**interfaz IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

En el modo de servidor de fotogramas, este atributo permite que el motor multimedia use la aceleración de hardware para la decodificación de vídeo y el procesamiento de vídeo. Si no se establece el atributo, el motor de medios usa la decodificación y el procesamiento de software.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




