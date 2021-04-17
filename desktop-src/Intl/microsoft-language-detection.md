---
description: El servicio de detección de lenguaje ELS se llama Microsoft Detección de idioma. Este servicio usa tecnología Microsoft-patentada para permitir que las aplicaciones detecten el idioma en el que se escribe el texto específico.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft Detección de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687089"
---
# <a name="microsoft-language-detection"></a>Microsoft Detección de idioma

El servicio de detección de lenguaje ELS se llama Microsoft Detección de idioma. Este servicio usa tecnología Microsoft-patentada para permitir que las aplicaciones detecten el idioma en el que se escribe el texto específico.

## <a name="input-to-microsoft-language-detection"></a>Entrada a Microsoft Detección de idioma

La entrada del servicio Microsoft Detección de idioma es UTF-16 (formato normalizado C). El servicio tiene que determinar el idioma de este texto.

## <a name="output-of-microsoft-language-detection"></a>Salida de Microsoft Detección de idioma

El servicio Microsoft Detección de idioma recupera los lenguajes de lista de cadenas UTF-16 con formato del registro y terminadas en null, representados por sus nombres, separados por delimitadores de caracteres null. La lista se ordena por relevancia. Para la mayoría de los idiomas, se usan nombres neutros. Sin embargo, para algunos, por ejemplo, Sr-Cyrl, Sr-Latn, ZH-hant y ZH-Hans, se usan nombres completos.

## <a name="microsoft-language-detection-operation"></a>Operación de Microsoft Detección de idioma

El servicio Microsoft Detección de idioma comprueba el script Unicode del texto proporcionado por la aplicación. Segmenta el texto en función de los scripts que detecta y, a continuación, determina el idioma en el que se escribe cada segmento. Si un script indica un solo idioma, se garantiza que el idioma está presente en la lista de resultados de los idiomas. El servicio utiliza un algoritmo patentado para determinar la relevancia de cada idioma admitido.

## <a name="microsoft-language-detection-guid"></a>GUID de Microsoft Detección de idioma

El GUID del servicio Microsoft Detección de idioma se declara en Elssrvc. h, tal como se muestra en el código siguiente.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los servicios lingüísticos extendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



