---
title: Implementación del código DSP
description: Implementación del código DSP
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- Complementos de Windows Media Player, procesamiento de señal digital (DSP)
- complementos, procesamiento de señal digital (DSP)
- Complementos de procesamiento de señal digital, implementar código
- Complementos DSP, implementar código
- Complementos de procesamiento de señal digital, modificar código de ejemplo
- Complementos DSP, modificar código de ejemplo
- Complementos de DSP de audio, implementar código
- Complementos de DSP de vídeo, implementar código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9e17dad39a4ba0ebe79e31d9f3eead843d7f81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695352"
---
# <a name="implementing-your-dsp-code"></a>Implementación del código DSP

Una vez que haya creado el complemento DSP de ejemplo, puede modificar el código para crear su propio complemento DSP de Windows Media Player. Los métodos que se cambian y los que se pueden dejar como dependen de los siguientes factores:

-   El número de propiedades que desea permitir que el usuario cambie. Seguramente querrá cambiar la implementación de la página de propiedades predeterminada para que se ajuste a sus necesidades, y puede que tenga que agregar propiedades adicionales.
-   Si el complemento de DSP necesita asignar recursos de streaming. El complemento puede requerir búferes adicionales.
-   Si el complemento de DSP de audio debe seguir generando datos después de que Windows Media Player haya dejado de proporcionar datos en el búfer de entrada.

En las secciones siguientes se usa el código de ejemplo de complemento DSP generado por el Asistente para complementos de Windows Media Player para ilustrar conceptos importantes. Puede que le resulte útil abrir Microsoft Visual Studio y generar primero el código de ejemplo para que pueda hacer referencia a él mientras lee esta sección. Para obtener más información acerca de cómo usar el Asistente para complementos de Media Player de Windows, consulte [crear un complemento DSP](building-a-dsp-plug-in.md).



| Sección                                                                    | Descripción                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementar un complemento de DSP de audio](implementing-an-audio-dsp-plug-in.md) | Describe lo que necesita saber para crear su propio complemento de DSP de audio basado en el ejemplo generado por el asistente. |
| [Implementación de un complemento DSP de vídeo](implementing-a-video-dsp-plug-in.md)   | Describe lo que necesita saber para crear su propio complemento de DSP de vídeo basado en el ejemplo generado por el asistente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




