---
description: Ejemplo de \_ AudioDelay de MFT
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468602"
---
# <a name="mft_audiodelay-sample"></a>Ejemplo de \_ AudioDelay de MFT

Muestra cómo implementar un efecto de audio como una transformación Media Foundation (MFT). El retraso de audio MFT acepta audio PCM como entrada, aplica un efecto de retraso (eco) y genera los datos de audio modificados.

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes Microsoft Media Foundation interfaces:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

El ejemplo AudioDelay de MFT \_ compila un archivo DLL que es un servidor COM para MFT. Antes de usar MFT, debe registrar el archivo DLL. Puede usar la herramienta TopoEdit para compilar una topología que incluya el MFT de retraso de audio. Para obtener más información sobre TopoEdit, vea [TopoEdit](topoedit.md). También puede modificar el ejemplo [de PlaybackFX](/previous-versions//bb970336(v=vs.85)) para usar MFT. Deberá modificar la función AddBranchToPartialTopology en Player.cpp. Cambie la siguiente línea de:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

A:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

El valor CLSID DelayMFT se declara en el archivo de encabezado AudioDelayUuids.h en la carpeta de ejemplo \_ \_ AudioDelay de MFT.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de GitHub Windows ejemplos clásicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Ejemplo de escala de grises de MFT \_](mft-grayscale-sample.md)
</dt> <dt>

[Escribir un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 
