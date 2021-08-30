---
title: Variables para realizar el procesamiento
description: Variables para realizar el procesamiento
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Reproductor de Windows Media complementos,método DoProcessOutput de ejemplo echo
- plug-ins,Echo sample DoProcessOutput (método)
- complementos de procesamiento de señales digitales, método DoProcessOutput de ejemplo de eco
- Complementos DE DSP, método DoProcessOutput de ejemplo de Eco
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, variables de procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f856808c1e9a00602fe3d2fe03d4255fd79bcfeb44c2021f2434ea670706cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001345"
---
# <a name="variables-to-perform-processing"></a>Variables para realizar el procesamiento

Las variables miembro para controlar el búfer de retraso tratan con **cantidades BYTE;** son punteros **BYTE** y un entero que almacena un recuento de bytes. Esto es ideal para procesar audio de 8 bits, ya que una muestra de 8 bits se ajusta perfectamente a un byte de memoria. Sin embargo, al procesar audio de 16 bits,  es más conveniente convertirlos en punteros cortos, por lo que el procesamiento puede producirse dos bytes a la vez.

El código de ejemplo siguiente asigna los nuevos punteros de 16 bits y agrega una variable de puntero que almacena la dirección del final del búfer de retraso. Insértelo en la sección "caso 16" justo antes del punto de entrada del bucle:


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



El código para el procesamiento de 8 bits también asigna una variable que almacena la dirección del final del búfer de retraso. Almacenar este valor facilita la prueba de si el puntero de búfer de retraso móvil ha alcanzado el final del búfer de retraso. El código de ejemplo siguiente calcula el valor:


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




