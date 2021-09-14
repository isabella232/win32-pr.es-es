---
description: En esta sección se describe cómo escribir una transformación de Media Foundation personalizada (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Escritura de un MFT personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363538"
---
# <a name="writing-a-custom-mft"></a>Escritura de un MFT personalizado

En esta sección se describe cómo escribir una transformación de Media Foundation personalizada (MFT).

## <a name="mft-checklist"></a>Lista de comprobación de MFT

Al implementar un MFT personalizado, use la siguiente lista de comprobación para determinar los requisitos:




| | | Todas las MTA | Todas las MTA deben implementar <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>MFTransform</strong></a>.<br /> En los temas siguientes se proporciona más información sobre la implementación de esta interfaz:<ul><li><a href="basic-mft-processing-model.md">Modelo básico de procesamiento de MFT</a></li><li><a href="time-stamps-and-durations.md">Marcas de tiempo y duraciones</a></li><li><a href="handling-stream-changes.md">Control de cambios de flujo</a></li></ul><br /> | | Codificadores y descodificadores | Requisitos: consulte <a href="implementing-a-codec-mft.md">Implementación de un códec MFT.</a><br /> Recomendado: <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>implemente IMFQualityAdvise</strong></a> o <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>para admitir notificaciones de calidad de servicio (QoS).<br /> | | Descodificadores de vídeo y procesadores de vídeo | Opcional: admite la aceleración de vídeo de DirectX.<br /><ul><li><a href="direct3d-aware-mfts.md">MTA con direct3D</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">Compatibilidad con DXVA 2.0 en Media Foundation</a></li></ul> | | Códecs de hardware | Vea Hardware MFT ( <a href="hardware-mfts.md">MTA de hardware).</a> | | Para que el MFT sea reconocible por las aplicaciones... | Vea <a href="registering-and-enumerating-mfts.md">Registrar y enumerar MTA.</a> | | Procesamiento de datos asincrónico | El modelo MFT predeterminado usa llamadas sincrónicas (bloqueo) para procesar datos. Para algunas MTA, el procesamiento asincrónico puede ser más eficaz. Sin embargo, también es más complejo de implementar.<br /> Para obtener más información, vea <a href="asynchronous-mfts.md">MFT asincrónicos.</a><br /> | | Control de velocidad, modo de truco o reproducción inversa | Vea <a href="implementing-rate-control.md">Implementing Rate Control</a>. | | Si el MFT crea subprocesos... | Implemente <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>la interfaz IMFRealTimeClient.</strong></a> | | Si el MFT tiene restricciones de licencia... | Considere la posibilidad de usar el mecanismo de campo de uso. Vea <a href="field-of-use-restrictions.md">Restricciones de campo de uso.</a> | | Si va a portar un objeto multimedia directX existente (DMO).. | Consulte <a href="comparison-of-mfts-and-dmos.md">Comparación de MTO y DMA.</a> | 




 

Esta sección contiene los siguientes temas:

-   [Marcas de tiempo y duraciones](time-stamps-and-durations.md)
-   [Control de cambios de flujo](handling-stream-changes.md)
-   [Implementación de un MFT de códec](implementing-a-codec-mft.md)
-   [MTA con direct3D](direct3d-aware-mfts.md)
-   [MTA de hardware](hardware-mfts.md)
-   [Codec Codec (Códec de me](codec-merit.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




