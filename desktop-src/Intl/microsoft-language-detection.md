---
description: El servicio de detección de idioma ELS se denomina Microsoft Detección de idioma. Este servicio usa tecnología de microsoft para permitir que las aplicaciones detecten el idioma en el que se escribe texto específico.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft Detección de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c4c4df0484287ef8bebcfdb2f395212b1985b282b7391d6c047dfb98d2ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788385"
---
# <a name="microsoft-language-detection"></a>Microsoft Detección de idioma

El servicio de detección de idioma ELS se denomina Microsoft Detección de idioma. Este servicio usa tecnología de microsoft para permitir que las aplicaciones detecten el idioma en el que se escribe texto específico.

## <a name="input-to-microsoft-language-detection"></a>Entrada a Microsoft Detección de idioma

La entrada al servicio microsoft Detección de idioma es texto UTF-16 (formato normalizado C). El servicio tiene que determinar el idioma de este texto.

## <a name="output-of-microsoft-language-detection"></a>Salida de Microsoft Detección de idioma

El servicio microsoft Detección de idioma recupera una cadena UTF-16 terminada en doble null con formato de registro, representada por sus nombres, separada por delimitadores de caracteres NULL. La lista se ordena por relevancia. En la mayoría de los idiomas, se usan nombres neutros. Sin embargo, para algunos, por ejemplo, sr-Cyrl, sr-Latn, zh-Hant y zh-Hans, se usan nombres completos.

## <a name="microsoft-language-detection-operation"></a>Operación de Detección de idioma Microsoft

El servicio Detección de idioma microsoft comprueba el script Unicode del texto proporcionado por la aplicación. Segmenta el texto en función de los scripts que detecta y, a continuación, determina el idioma en el que se escribe cada segmento. Si un script indica un idioma único, se garantiza que el idioma esté presente en la lista de salida de idiomas. El servicio usa un algoritmo de compresión para determinar la relevancia de cada idioma admitido.

## <a name="microsoft-language-detection-guid"></a>GUID Detección de idioma Microsoft

El GUID del servicio de Detección de idioma Microsoft se declara en Elssrvc.h, como se muestra en el código siguiente.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los servicios lingüísticos extendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



