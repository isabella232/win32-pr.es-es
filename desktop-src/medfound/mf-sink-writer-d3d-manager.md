---
description: Contiene un puntero al objeto DXGI Administrador de dispositivos del escritor receptor.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: MF_SINK_WRITER_D3D_MANAGER atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706287b6001ba52c8bf5ba8a19326948afcf4f7f7569c606507115f484c46f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714315"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>Atributo MF \_ SINK \_ WRITER \_ D3D \_ MANAGER

Contiene un puntero a la Administrador de dispositivos DXGI para [el escritor de receptores.](sink-writer.md)

## <a name="data-type"></a>Tipo de datos

**IMFDXGIDeviceManager \* *_ almacenado como _* IUnknown\***

## <a name="remarks"></a>Comentarios

El valor de este atributo es un puntero a la [**interfaz IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

Use este atributo para proporcionar un dispositivo Direct3D para los codificadores de vídeo o receptores multimedia cargados por el escritor de receptores.

Use este atributo con las siguientes funciones:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Escritor de receptores](sink-writer.md)
</dt> </dl>

 

 




