---
description: Contiene un puntero al Administrador de dispositivos de Microsoft Direct3D para el lector de origen.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: MF_SOURCE_READER_D3D_MANAGER atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910197"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>\_Atributo de \_ Administrador de D3D de lector de origen MF \_ \_

Contiene un puntero al Administrador de dispositivos de Microsoft [Direct3D](direct3d-device-manager.md) para el [lector de origen](source-reader.md).

## <a name="data-type"></a>Tipo de datos

**IDirect3DDeviceManager9 \* o IMFDXGIDeviceManager \*** almacenado como **IUnknown \** _

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

El valor de este atributo puede ser un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) o a un [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).

Use este atributo para proporcionar un dispositivo Direct3D para cualquier descodificador de vídeo cargado por el lector de origen. Si establece este atributo y el descodificador es compatible con Microsoft DirectX video Acceleration (DXVA), el lector de origen usa el dispositivo Direct3D para asignar búferes de vídeo. Estos búferes son compatibles con el procesador de vídeo DXVA 2. (Consulte el [procesamiento de vídeo de DXVA](dxva-video-processing.md)).

Utilice este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Normalmente se establece este atributo si se usa el lector de origen para obtener fotogramas de vídeo descodificados y usar Direct3D para mostrar los fotogramas. Al establecer este atributo, el descodificador podrá usar DXVA.

No establecería este atributo si:

-   Está usando el lector de origen para procesar solo audio y no vídeo.
-   Está obteniendo vídeo comprimido del lector de origen. En ese caso, el lector de origen no crea un descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




