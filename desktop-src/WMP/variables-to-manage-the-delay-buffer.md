---
title: Variables para administrar el búfer de retraso
description: Variables para administrar el búfer de retraso
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Complementos de Windows Media Player, echo ejemplo de recursos de streaming
- complementos, echo ejemplo de recursos de streaming
- Complementos de procesamiento de señal digital, echo ejemplo de recursos de streaming
- Complementos DSP, echo ejemplo de recursos de streaming
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo de complemento DSP de eco, búfer de retraso
- búfer de retraso
- búferes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268941"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variables para administrar el búfer de retraso

Debe agregar las declaraciones de las variables de miembro que necesita para administrar el búfer de retraso. Agregue las declaraciones siguientes a ECHO. h en la sección "privada":


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

 

 




