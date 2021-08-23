---
title: Variables para administrar el búfer de retraso
description: Variables para administrar el búfer de retraso
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Reproductor de Windows Media complementos, recursos de streaming de ejemplo de eco
- complementos, recursos de streaming de ejemplo de eco
- complementos de procesamiento de señales digitales, recursos de streaming de ejemplo de eco
- Complementos DE DSP, recursos de streaming de ejemplo de eco
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo del complemento DSP de eco, búfer de retraso
- búfer de retraso
- búferes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571745"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variables para administrar el búfer de retraso

Debe agregar las declaraciones de las variables miembro que necesita para administrar el búfer de retraso. Agregue las siguientes declaraciones a Echo.h en la sección "private":


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Agregue el código siguiente al constructor CEcho para inicializar las variables de búfer de retraso:


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




