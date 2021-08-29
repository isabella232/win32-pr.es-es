---
description: Contiene un puntero a la cuenta de Microsoft Direct3D Administrador de dispositivos lector de origen.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: MF_SOURCE_READER_D3D_MANAGER atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19b4f90713d6eb0529e51657d3f5a649394c3458c61d6cce2974b2214d9a202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955129"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>Atributo \_ MF SOURCE READER \_ \_ D3D \_ MANAGER

Contiene un puntero a microsoft [direct3D Administrador de dispositivos](direct3d-device-manager.md) para el [lector de origen.](source-reader.md)

## <a name="data-type"></a>Tipo de datos

**IDirect3DDeviceManager9 \* o IMFDXGIDeviceManager \*** almacenados como **IUnknown \***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentarios

El valor de este atributo puede ser un puntero a la [**interfaz IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) o [**a UN VALOR DEDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

Use este atributo para proporcionar un dispositivo Direct3D para los descodificadores de vídeo cargados por el lector de origen. Si establece este atributo y el descodificador admite la aceleración de vídeo de Microsoft DirectX (DXVA), el lector de origen usa el dispositivo Direct3D para asignar búferes de vídeo. Estos búferes son compatibles con el procesador de vídeo DXVA 2. (Consulte [Procesamiento de vídeo DXVA).](dxva-video-processing.md)

Use este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Normalmente, establecería este atributo si usa el lector de origen para obtener fotogramas de vídeo descodificados y usar Direct3D para mostrar los fotogramas. Al establecer este atributo, el descodificador puede usar DXVA.

No establecería este atributo si:

-   Está usando el lector de origen para procesar solo audio y no vídeo.
-   Se está comprimiendo el vídeo desde el lector de origen. En ese caso, el lector de origen no crea un descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




