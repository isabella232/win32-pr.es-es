---
description: En esta sección se describe cómo escribir una transformación de Media Foundation personalizada (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Escribir una MFT personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910189"
---
# <a name="writing-a-custom-mft"></a>Escribir una MFT personalizada

En esta sección se describe cómo escribir una transformación de Media Foundation personalizada (MFT).

## <a name="mft-checklist"></a>Lista de comprobación de MFT

Cuando implemente un MFT personalizado, use la siguiente lista de comprobación para determinar los requisitos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Todos los MFTs</td>
<td>Todos los MFTs deben implementar <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.<br/> En los temas siguientes se proporciona más información acerca de la implementación de esta interfaz:
<ul>
<li><a href="basic-mft-processing-model.md">Modelo básico de procesamiento de MFT</a></li>
<li><a href="time-stamps-and-durations.md">Marcas de tiempo y duraciones</a></li>
<li><a href="handling-stream-changes.md">Control de los cambios de flujo</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Codificadores y descodificadores</td>
<td>Requisitos: vea <a href="implementing-a-codec-mft.md">implementación de un MFT de códec</a>.<br/> Recomendado: implemente <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> o <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>para admitir notificaciones de calidad de servicio (QoS).<br/></td>
</tr>
<tr class="odd">
<td>Descodificadores de vídeo y procesadores de vídeo</td>
<td>Opcional: compatibilidad con la aceleración de vídeo de DirectX.<br/>
<ul>
<li><a href="direct3d-aware-mfts.md">MFTs compatible con Direct3D</a></li>
<li><a href="supporting-dxva-2-0-in-media-foundation.md">Compatibilidad con DXVA 2,0 en Media Foundation</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Códecs de hardware</td>
<td>Consulte <a href="hardware-mfts.md">hardware MFTs</a>.</td>
</tr>
<tr class="odd">
<td>Para que las aplicaciones puedan detectar su MFT...</td>
<td>Consulte <a href="registering-and-enumerating-mfts.md">registro y enumeración de MFTs</a>.</td>
</tr>
<tr class="even">
<td>Procesamiento de datos asincrónicos</td>
<td>El modelo de MFT predeterminado usa llamadas sincrónicas (bloqueo) para procesar los datos. En algunos MFTs, el procesamiento asincrónico puede ser más eficaz. Sin embargo, también es más difícil de implementar.<br/> Para obtener más información, consulte <a href="asynchronous-mfts.md">MFTs asincrónico</a>.<br/></td>
</tr>
<tr class="odd">
<td>Control de velocidad, modo de truco o reproducción inversa</td>
<td>Vea <a href="implementing-rate-control.md">implementar el control de tasa</a>.</td>
</tr>
<tr class="even">
<td>Si su MFT crea subprocesos...</td>
<td>Implemente la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</td>
</tr>
<tr class="odd">
<td>Si su MFT tiene restricciones de licencia...</td>
<td>Considere la posibilidad de usar el mecanismo de campo de uso. Vea el <a href="field-of-use-restrictions.md">campo de restricciones de uso</a>.</td>
</tr>
<tr class="even">
<td>Si va a migrar un objeto multimedia de DirectX existente (DMO)...</td>
<td>Vea <a href="comparison-of-mfts-and-dmos.md">comparación de MFTs y DMOs</a>.</td>
</tr>
</tbody>
</table>



 

Esta sección contiene los siguientes temas:

-   [Marcas de tiempo y duraciones](time-stamps-and-durations.md)
-   [Control de los cambios de flujo](handling-stream-changes.md)
-   [Implementar un MFT de códec](implementing-a-codec-mft.md)
-   [MFTs compatible con Direct3D](direct3d-aware-mfts.md)
-   [MFTs de hardware](hardware-mfts.md)
-   [Mérito del códec](codec-merit.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




