---
title: Interpolación de fotogramas
description: Interpolación de fotogramas
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows SDK de formato multimedia, interpolación de fotogramas
- códecs, interpolación de fotogramas
- interpolación de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b10691bd2a1f3e6257810efd1e243d099cd4cfa85f0b2522369786602792614
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007015"
---
# <a name="frame-interpolation"></a>Interpolación de fotogramas

La interpolación de fotogramas es el proceso de crear fotogramas de vídeo intermedios basados en los datos de dos fotogramas consecutivos de vídeo codificado. En efecto, la interpolación de fotogramas aumenta la [*velocidad*](wmformat-glossary.md) de fotogramas del vídeo codificado en el momento de la descodificación. Puede usar la interpolación de fotogramas para mejorar la subilidad de la reproducción de secuencias de vídeo con velocidades de fotogramas bajas.

Dado que se trata de una característica de codificación, no implica ninguna opción de codificación especial y no agrega ninguna sobrecarga al contenido. La interpolación de fotogramas se especifica como una configuración de salida en el objeto de lector.

Solo el códec Windows Media Video 9 admite la interpolación de fotogramas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Salida Configuración**](output-settings.md)
</dt> </dl>

 

 




