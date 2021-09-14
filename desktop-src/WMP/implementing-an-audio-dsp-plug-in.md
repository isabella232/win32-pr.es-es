---
title: Implementación de un complemento dsp de audio
description: Implementación de un complemento dsp de audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Reproductor de Windows Media complementos,DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señales digitales, implementar código
- Complementos de DSP, implementar código
- complementos de procesamiento de señales digitales, modificación del código de ejemplo
- Complementos de DSP, modificar código de ejemplo
- complementos de procesamiento de señal digital, implementación de audio
- Complementos de DSP, implementación de audio
- complementos de DSP de audio, implementar código
- complementos DSP de audio, modificar código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068430"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementación de un complemento dsp de audio

Para crear un Reproductor de Windows Media de DSP que procese el audio, deberá modificar el código de ejemplo en la función **denominada DoProcessOutput**. **Se llama a DoProcessOutput** cada Reproductor de Windows Media llama correctamente a **IMediaObject::P rocessOutput**. Es la función que realiza las tareas de procesamiento de señales digitales que producen el resultado de audio que el complemento DSP está diseñado para generar.

El procesamiento de una secuencia de audio es como controlar un evento con tiempo. **Se llamará a DoProcessOutput** repetidamente y a intervalos específicos. Cada vez que se ejecuta el código, tendrá que procesar un número específico de bytes de datos. **DoProcessOutput** contiene los parámetros siguientes:



| Parámetro          | Descripción                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Se trata de **un puntero BYTE** al búfer donde la implementación de **DoProcessOutput** debe copiar los datos procesados. |
| *pbInputData*      | Se trata de un **puntero BYTE** constante al búfer que contiene los datos que se procesarán.                               |
| *cbBytesToProcess* | Se trata de **un valor DWORD** que contiene un recuento del número de bytes del búfer de entrada que se va a procesar.             |



 

En las secciones siguientes se proporcionan detalles sobre cómo modificar el código generado por el Asistente para complementos de Reproductor de Windows Media para crear su propio complemento DSP de audio:

-   [Implementación de DoProcessOutput](implementing-doprocessoutput.md)
-   [Agregar propiedades al complemento DSP de audio de ejemplo](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementar la página de propiedades para un complemento DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Cambiar la propiedad del complemento DSP de audio de ejemplo](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Acerca de la discontinuidad](about-discontinuity.md)
-   [Acerca de la asignación de recursos de streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos de DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




