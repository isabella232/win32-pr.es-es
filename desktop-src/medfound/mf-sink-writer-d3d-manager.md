---
description: Contiene un puntero al Administrador de dispositivos de DXGI para el escritor del receptor.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: MF_SINK_WRITER_D3D_MANAGER atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716951"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_Atributo de \_ Administrador de D3D del escritor de receptor MF \_ \_

Contiene un puntero al Administrador de dispositivos de DXGI para el [escritor del receptor](sink-writer.md).

## <a name="data-type"></a>Tipo de datos

**IMFDXGIDeviceManager \** _ almacenado como _*IUnknown \**_

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Use este atributo para proporcionar un dispositivo Direct3D para cualquier codificador de vídeo o receptor de medios cargados por el escritor del receptor.

Utilice este atributo con las siguientes funciones:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Escritor de receptor](sink-writer.md)
</dt> </dl>

 

 




