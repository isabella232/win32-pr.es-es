---
title: Implementar un complemento de DSP de audio
description: Implementar un complemento de DSP de audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, implementar código
- Complementos DSP, implementar código
- Complementos de procesamiento de señal digital, modificar código de ejemplo
- Complementos DSP, modificar código de ejemplo
- Complementos de procesamiento de señal digital, implementación de audio
- Complementos DSP, implementación de audio
- Complementos de DSP de audio, implementar código
- Complementos de DSP de audio, modificación del código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076039"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementar un complemento de DSP de audio

Para crear un complemento DSP de Windows Media Player que procese audio, deberá modificar el código de ejemplo de la función denominada **DoProcessOutput**. Se llama a **DoProcessOutput** cada vez que Windows Media Player llama correctamente a **IMediaObject::P rocessoutput**. Es la función que realiza las tareas de procesamiento de señal digital que producen el resultado audible que el complemento de DSP pretende producir.

El procesamiento de una secuencia de audio es como controlar un evento con hora. Se llamará a **DoProcessOutput** repetidamente y a intervalos específicos. Cada vez que se ejecuta el código, tendrá que procesar un número específico de bytes de datos. **DoProcessOutput** contiene los siguientes parámetros:



| Parámetro          | Descripción                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Se trata de un puntero de **bytes** al búfer en el que la implementación de **DoProcessOutput** debe copiar sus datos procesados. |
| *pbInputData*      | Se trata de un puntero de **byte** constante al búfer que contiene los datos que se van a procesar.                               |
| *cbBytesToProcess* | Es un valor **DWORD** que contiene un recuento del número de bytes en el búfer de entrada que se va a procesar.             |



 

En las secciones siguientes se proporcionan detalles sobre cómo modificar el código generado por el Asistente para complementos de Media Player de Windows para crear su propio complemento de DSP de audio:

-   [Implementación de DoProcessOutput](implementing-doprocessoutput.md)
-   [Agregar propiedades al complemento DSP de audio de ejemplo](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementar la página de propiedades de un complemento DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Cambio de la propiedad del complemento DSP de audio de ejemplo](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Acerca de la discontinuidad](about-discontinuity.md)
-   [Acerca de la asignación de recursos de streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




