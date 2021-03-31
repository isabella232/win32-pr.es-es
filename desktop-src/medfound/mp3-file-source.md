---
description: El origen de archivo MP3 analiza los archivos MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origen de archivo MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155344"
---
# <a name="mp3-file-source"></a>Origen de archivo MP3

El origen de archivo MP3 analiza los archivos MP3.

El origen de archivo MP3 genera búferes que contienen fotogramas de audio MPEG-1. No descodifica el audio.

## <a name="file-extensions-and-mime-types"></a>Extensiones de archivo y tipos MIME

El origen de archivo MP3 es el origen de medios predeterminado para la siguiente extensión de nombre de archivo:

-   .mp3

También es el origen de medios predeterminado para los siguientes tipos MIME.

-   audio/MPEG
-   audio/x-mp3
-   audio/x-MPEG

## <a name="media-types"></a>Tipos de medios

El tipo de medio que ofrece el origen de archivos MP3 contiene los siguientes atributos.



| Atributo                                                                                    | Descripción                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                                    | Igual a **MFMediaType \_ audio**.                                                                                                                   |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | Igual a **MFAudioFormat \_ mp3** o **MFAudioFormat \_ MPEG**.                                                                                        |
| [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Número promedio de bytes por segundo.                                                                                                                |
| [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)             | Igual a 1.                                                                                                                                        |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | Número de canales de audio.                                                                                                                          |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)      | Número de muestras de audio por segundo.                                                                                                                |
| [**datos de usuario de MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                                      | Contiene la parte de una estructura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) que aparece después del miembro de **WFX** de la estructura. |



 

## <a name="interfaces"></a>Interfaces

El origen de archivo MP3 expone las siguientes interfaces a través de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Además, expone las siguientes interfaces a través de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID de servicio</th>
<th>Interfaz</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
<blockquote>
[!Note]<br />
Consulte <a href="shell-metadata-providers.md">proveedores de metadatos de Shell</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                           |
| Archivo DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Orígenes y receptores de medios](media-sources-and-sinks.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
