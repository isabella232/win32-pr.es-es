---
title: Escritura de velocidad de bits variable Secuencias
description: Escritura de velocidad de bits variable Secuencias
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Formato de sistemas avanzados (ASF), escribir secuencias VBR
- ASF (formato de sistemas avanzados), escritura de secuencias VBR
- velocidad de bits variable (VBR), escritura de secuencias
- VBR (velocidad de bits variable), escritura de secuencias
- streams,writing VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694774613ada8b4be05eab55be3213898d423d3b6ac4438204d149a0bd606c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930265"
---
# <a name="writing-variable-bit-rate-streams"></a>Escritura de velocidad de bits variable Secuencias

Las secuencias de velocidad de bits variable (VBR) se escriben de la misma manera que las secuencias de velocidad de bits constante (CBR). La única diferencia está en el procesamiento realizado internamente por el escritor y los códecs. Sin embargo, la VBR basada en velocidad de bits (restringida y sin restricciones) requiere un paso de preprocesamiento en el escritor.

Debe comprobar el valor devuelto de la primera llamada que realice a [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) para cada secuencia. Si el código de error devuelto es NS \_ E \_ INVALID NUM \_ \_ PASSES, la secuencia requiere un paso de preprocesamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de Two-Pass codificación**](using-two-pass-encoding.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




