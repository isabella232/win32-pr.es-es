---
description: Configuración de la descodificación de audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configuración de la descodificación de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808149"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configuración de la descodificación de audio (Microsoft Media Foundation)

Descodificar el contenido Windows Media Audio es mucho más fácil que codificarlo. Después de crear un objeto de descodificador de audio, establezca el tipo de entrada mediante el método **IMediaObject:: SetInputType** o **IMFTransform:: SetInputType** . El tipo de medio que se usa para la entrada del descodificador debe coincidir con el tipo de salida que se usó al codificar el contenido. Esto incluye los datos de formato extendido anexados a la estructura **WAVEFORMATEX** . Debe asegurarse de que estos datos son correctos, porque el descodificador no puede procesar ejemplos sin él.

Después de establecer el tipo de entrada, puede configurar las características del descodificador que desee usar. Las características del descodificador, como las que se usan para la codificación, se establecen mediante los métodos de **IPropertyBag** o **IPropertyStore**.

Una vez que se establece el tipo de entrada y se configuran todas las características del descodificador, se pueden enumerar los tipos de salida admitidos por el descodificador realizando llamadas a **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



