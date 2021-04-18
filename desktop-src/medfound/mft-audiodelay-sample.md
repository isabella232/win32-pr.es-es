---
description: Ejemplo de AudioDelay de MFT \_
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Ejemplo de MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659837"
---
# <a name="mft_audiodelay-sample"></a>Ejemplo de AudioDelay de MFT \_

Muestra cómo implementar un efecto de audio como una transformación de Media Foundation (MFT). El MFT de retraso de audio acepta el audio PCM como entrada, aplica un efecto de retraso (eco) y genera los datos de audio modificados.

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

El \_ ejemplo AudioDelay de MFT crea un archivo DLL que es un servidor com para la MFT. Antes de usar la MFT, debe registrar el archivo DLL. Puede usar la herramienta TopoEdit para crear una topología que incluya el MFT de retardo de audio. Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md). También puede modificar el [ejemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)) para usar la MFT. Tendrá que modificar la función AddBranchToPartialTopology en Player. cpp. Cambie la siguiente línea de:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

Por:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

El valor CLSID \_ DelayMFT se declara en el archivo de encabezado AudioDelayUuids. h de la \_ carpeta de ejemplo MFT AudioDelay.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[\_Ejemplo de escala de grises de MFT](mft-grayscale-sample.md)
</dt> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 
