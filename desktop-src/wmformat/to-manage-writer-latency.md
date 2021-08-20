---
title: Para administrar la latencia del escritor
description: Para administrar la latencia del escritor
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Formato de sistemas avanzados (ASF), administración de la latencia del escritor
- ASF (formato de sistemas avanzados), administración de la latencia del escritor
- Formato de sistemas avanzados (ASF), latencia del escritor
- ASF (formato de sistemas avanzados), latencia del escritor
- latencia del escritor
- latency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0adb18814cc8153ae81ed9517834d62345f18b61f51de6aacd38e9028699331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845485"
---
# <a name="to-manage-writer-latency"></a>Para administrar la latencia del escritor

El escritor tarda tiempo en procesar ejemplos. La cantidad de tiempo entre pasar una muestra de entrada y la escritura de una muestra de salida se denomina latencia del escritor. Varios factores contribuyen a la latencia del escritor y puede reducirla de varias maneras.

El factor más obvio implicado en la latencia del escritor es el tiempo que se tarda en comprimir una muestra. En la mayoría de las circunstancias, tendrá poco o ningún control sobre esto. Si el ancho de banda no es una gran preocupación, puede reducir la latencia con menos compresión. Por supuesto, puede lograr la menor latencia pasando muestras que ya están comprimidas.

El siguiente factor, y uno sobre el que normalmente tiene control, es el orden en el que se pasan las muestras al lector. Puede lograr una mejor latencia pasando muestras en orden de tiempo de presentación y asegurándose de que las muestras de entrada están bien sincronizadas entre todos los flujos de entrada. Cuanto mayor sea la discrepancia en los tiempos de presentación entre los ejemplos de diferentes secuencias, mayor será la latencia. Puede establecer un máximo para la discrepancia entre los ejemplos de entrada llamando a [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




