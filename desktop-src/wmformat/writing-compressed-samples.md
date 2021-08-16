---
title: Escribir ejemplos comprimidos
description: Escribir ejemplos comprimidos
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Formato de sistemas avanzados (ASF), escribir ejemplos comprimidos
- ASF (formato de sistemas avanzados), escribir ejemplos comprimidos
- Formato de sistemas avanzados (ASF), pasar ejemplos comprimidos
- ASF (formato de sistemas avanzados), pasar muestras comprimidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaa6bf5298e465716fe7a60eb5de2459f09be405611ac7322b534804bbbc997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843659"
---
# <a name="writing-compressed-samples"></a>Escribir ejemplos comprimidos

Para algunas secuencias de audio o vídeo, es posible que desee pasar muestras que ya están comprimidas en lugar de pasar datos sin procesar. Esta característica se usa para copiar una secuencia existente o para escribir ejemplos comprimidos con un códec de terceros. El proceso de escritura de un ejemplo comprimido es idéntico a escribir un ejemplo sin comprimir, salvo que se usa [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) en lugar de [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para obtener más información sobre cómo escribir ejemplos sin comprimir, vea [Para escribir ejemplos.](to-write-samples.md)

Al escribir ejemplos comprimidos, para los perfiles CBR, el escritor quitará algunos ejemplos, si es necesario, para mantener el contenido dentro de los valores de velocidad de bits y ventana de búfer especificados. Para VBR, el escritor no quitará ejemplos, pero no hay ninguna manera de asegurarse de que los valores de la ventana de búfer y velocidad de bits serán correctos.

Si va a copiar una secuencia de un archivo a otro, siempre debe copiar el objeto de configuración de secuencia del perfil del archivo original al perfil del nuevo archivo. Esto garantiza que tiene la velocidad de bits correcta y la información de la ventana de búfer. Si copia una secuencia comprimida en una secuencia que tiene un conjunto de ventanas de búfer inferior, los ejemplos se descartarán durante la escritura de archivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




