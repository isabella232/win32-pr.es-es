---
title: Variables para realizar el procesamiento
description: Variables para realizar el procesamiento
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento de DSP de eco, variables de procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776644"
---
# <a name="variables-to-perform-processing"></a>Variables para realizar el procesamiento

Las variables miembro para controlar el búfer de retraso tratan las cantidades de **bytes** . son punteros de **bytes** y un entero que almacena un recuento de bytes. Esto es idóneo para procesar audio de 8 bits, ya que una muestra de 8 bits se ajusta perfectamente a un byte de memoria. Sin embargo, cuando se procesa audio de 16 bits, es más conveniente convertirlos en punteros **cortos** , por lo que el procesamiento puede producirse en dos bytes a la vez.

En el siguiente código de ejemplo se asignan los nuevos punteros de 16 bits y se agrega una variable de puntero que almacena la dirección del final del búfer de retraso. Insértelo en la sección "Case 16" justo antes del punto de entrada del bucle:


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



El código para el procesamiento de 8 bits también asigna una variable que almacena la dirección del final del búfer de retraso. El almacenamiento de este valor facilita la prueba de si el puntero de búfer de retraso móvil ha alcanzado el final del búfer de retraso. En el código de ejemplo siguiente se calcula el valor:


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




