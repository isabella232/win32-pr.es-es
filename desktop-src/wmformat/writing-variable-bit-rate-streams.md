---
title: Escribir secuencias de velocidad de bits variable
description: Escribir secuencias de velocidad de bits variable
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF), escribir secuencias VBR
- ASF (formato de sistemas avanzados), escritura de secuencias VBR
- velocidad de bits variable (VBR), escribir secuencias
- VBR (velocidad de bits variable), escribir secuencias
- secuencias, escribir VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788685"
---
# <a name="writing-variable-bit-rate-streams"></a>Escribir secuencias de velocidad de bits variable

Las secuencias de velocidad de bits variable (VBR) se escriben de la misma forma que las secuencias de velocidad de bits constante (CBR). La única diferencia es el procesamiento que realiza internamente el escritor y los códecs. Sin embargo, la VBR basada en la velocidad de bits (tanto restringida como sin restricciones) requiere un paso de preprocesamiento en el escritor.

Debe comprobar el valor devuelto por la primera llamada que realice a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) para cada secuencia. Si el código de error devuelto es NS \_ E \_ no válidos \_ \_ , la secuencia requiere un paso de preprocesamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de la codificación de Two-Pass**](using-two-pass-encoding.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




