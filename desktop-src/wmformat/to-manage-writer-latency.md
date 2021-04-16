---
title: Para administrar la latencia del escritor
description: Para administrar la latencia del escritor
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF), administración de la latencia del escritor
- ASF (formato de sistemas avanzados), administración de la latencia del escritor
- Advanced Systems Format (ASF), latencia del escritor
- ASF (formato de sistemas avanzados), latencia del sistema de escritura
- latencia del escritor
- latency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685676"
---
# <a name="to-manage-writer-latency"></a>Para administrar la latencia del escritor

El escritor tarda tiempo en procesar ejemplos. La cantidad de tiempo entre pasar una muestra de entrada y la escritura de un ejemplo de salida se denomina latencia del escritor. Una serie de factores contribuye a la latencia del escritor y se puede reducir de varias maneras.

El factor más obvio implicado en la latencia del escritor es el tiempo que se tarda en comprimir un ejemplo. En la mayoría de los casos, tendrá poco o ningún control sobre esto. Si el ancho de banda no es una preocupación importante, puede reducir la latencia usando menos compresión. Por supuesto, puede lograr la menor latencia pasando ejemplos que ya están comprimidos.

El siguiente factor, y otro sobre el que normalmente tiene el control, es el orden en el que se pasan los ejemplos al lector. Puede lograr una mejor latencia si pasa las muestras en orden de tiempo de presentación y garantiza que los ejemplos de entrada estén bien sincronizados entre todos los flujos de entrada. Cuanto mayor sea la discrepancia en el momento de la presentación entre los ejemplos de flujos diferentes, mayor será la latencia. Puede establecer un máximo para la discrepancia entre los ejemplos de entrada mediante una llamada a [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




