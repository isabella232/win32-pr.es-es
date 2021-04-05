---
title: Interpolación de fotogramas
description: Interpolación de fotogramas
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- SDK de Windows Media Format, interpolación de marcos
- códecs, interpolación de fotogramas
- interpolación de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077318"
---
# <a name="frame-interpolation"></a>Interpolación de fotogramas

La interpolación de fotogramas es el proceso de creación de fotogramas de vídeo intermedios basados en los datos de dos fotogramas consecutivos de vídeo codificado. En efecto, la interpolación de fotogramas aumenta la [*velocidad de fotogramas*](wmformat-glossary.md) del vídeo codificado en el momento de la descodificación. Puede usar la interpolación de fotogramas para mejorar la suavidad de la reproducción de secuencias de vídeo con velocidades de fotogramas bajas.

Dado que se trata de una característica de descodificación, no implica ninguna opción de codificación especial y no agrega ninguna sobrecarga al contenido. La interpolación de fotogramas se especifica como una configuración de salida en el objeto de lector.

Solo el códec de Windows Media Video 9 admite la interpolación de fotogramas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Configuración de salida**](output-settings.md)
</dt> </dl>

 

 




