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
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247137"
---
# <a name="writing-compressed-samples"></a>Escribir ejemplos comprimidos

Para algunas secuencias de audio o vídeo, es posible que desee pasar muestras que ya están comprimidas en lugar de pasar datos sin procesar. Esta característica se usa para copiar una secuencia existente o para escribir ejemplos comprimidos con un códec de terceros. El proceso de escritura de un ejemplo comprimido es idéntico a escribir un ejemplo sin comprimir, salvo que se usa [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) en lugar de [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para obtener más información sobre cómo escribir ejemplos sin comprimir, vea [Para escribir ejemplos.](to-write-samples.md)

Al escribir ejemplos comprimidos, para los perfiles CBR, el escritor quitará algunos ejemplos, si es necesario, para mantener el contenido dentro de los valores de velocidad de bits y ventana de búfer especificados. Para VBR, el escritor no quitará ejemplos, pero no hay ninguna manera de asegurarse de que los valores de la ventana de búfer y velocidad de bits serán correctos.

Si va a copiar una secuencia de un archivo a otro, siempre debe copiar el objeto de configuración de secuencia del perfil del archivo original al perfil del nuevo archivo. Esto garantiza que tiene la velocidad de bits correcta y la información de la ventana de búfer. Si copia una secuencia comprimida en una secuencia que tiene un conjunto de ventanas de búfer inferior, los ejemplos se descartarán durante la escritura de archivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




