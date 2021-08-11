---
description: El origen del archivo MP3 analiza los archivos MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origen del archivo MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b5649f1bdbc9d9b3dfa0af2f04878dfa64852af85ff8e829d4d2d4c4d20d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240110"
---
# <a name="mp3-file-source"></a>Origen del archivo MP3

El origen del archivo MP3 analiza los archivos MP3.

El origen del archivo MP3 genera búferes que contienen fotogramas de audio MPEG-1. No descodifica el audio.

## <a name="file-extensions-and-mime-types"></a>Extensiones de archivo y tipos MIME

El origen de archivo MP3 es el origen multimedia predeterminado para la siguiente extensión de nombre de archivo:

-   .mp3

También es el origen multimedia predeterminado para los siguientes tipos MIME.

-   audio/mpeg
-   audio/x-mp3
-   audio/x-mpeg

## <a name="media-types"></a>Tipos de medios

El tipo de medio que ofrece el origen del archivo MP3 contiene los siguientes atributos.



| Atributo                                                                                    | Descripción                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md)                                    | Es igual **a MFMediaType \_ Audio**.                                                                                                                   |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)                                           | Es igual **a MFAudioFormat \_ MP3** **o MFAudioFormat \_ MPEG**.                                                                                        |
| [**PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Número medio de bytes por segundo.                                                                                                                |
| [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)             | Igual a 1.                                                                                                                                        |
| [**CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT**](mf-mt-audio-num-channels-attribute.md)                   | Número de canales de audio.                                                                                                                          |
| [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)      | Número de muestras de audio por segundo.                                                                                                                |
| [**DATOS \_ DE USUARIO DE MF MT \_ \_**](mf-mt-user-data-attribute.md)                                      | Contiene la parte de una [**estructura MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) que aparece después del **miembro wfx** de la estructura. |



 

## <a name="interfaces"></a>Interfaces

El origen del archivo MP3 expone las interfaces siguientes a través [**de QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Además, expone las interfaces siguientes a través de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):



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
Vea <a href="shell-metadata-providers.md">Proveedores de metadatos de Shell.</a>
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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                           |
| Archivo DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Orígenes multimedia y receptores](media-sources-and-sinks.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
