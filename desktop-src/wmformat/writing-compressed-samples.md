---
title: Escribir ejemplos comprimidos
description: Escribir ejemplos comprimidos
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF), escribir ejemplos comprimidos
- ASF (formato de sistemas avanzados), escribir ejemplos comprimidos
- Advanced Systems Format (ASF), pasar ejemplos comprimidos
- ASF (formato de sistemas avanzados), pasar ejemplos comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487287"
---
# <a name="writing-compressed-samples"></a>Escribir ejemplos comprimidos

En el caso de algunas secuencias de audio o vídeo, es posible que desee pasar muestras que ya estén comprimidas en lugar de pasar datos sin procesar. Esta característica se usa para copiar un flujo existente o escribir ejemplos comprimidos con un códec de terceros. El proceso de escritura de un ejemplo comprimido es idéntico al de escribir un ejemplo sin comprimir, salvo que se usa [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) en lugar de [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para obtener más información sobre cómo escribir ejemplos sin comprimir, vea [para escribir ejemplos](to-write-samples.md).

Al escribir ejemplos comprimidos, para perfiles CBR, el escritor quitará algunos ejemplos, si es necesario, para mantener el contenido dentro de la velocidad de bits y los valores de la ventana de búfer especificados. En el caso de VBR, el sistema de escritura no quitará los ejemplos, pero no hay ninguna manera de asegurarse de que los valores de velocidad de bits y de la ventana de búfer serán correctos.

Si va a copiar una secuencia de un archivo a otro, debe copiar siempre el objeto de configuración de secuencia del perfil del archivo original en el perfil del nuevo archivo. Esto garantiza que tenga la información de la ventana de búfer y la velocidad de bits correcta. Si copia un flujo comprimido en una secuencia que tiene un conjunto de ventanas de búfer inferior, se quitarán los ejemplos durante la escritura del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




