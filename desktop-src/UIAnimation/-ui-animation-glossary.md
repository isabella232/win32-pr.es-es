---
title: Windows Glosario de animación
description: Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan Windows Animation Manager.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Windows Animación Windows animación , glosario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb477edcaa49aa8baff1bc628ca5d94c13dacc0e552137275ff1e92d8e4cfae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137398"
---
# <a name="windows-animation-glossary"></a>Windows Glosario de animación

Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan Windows Animation Manager.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animación** 
</dt> <dd>

Secuencia de imágenes fijas sintéticas y sucesivas que produce una sensación de movimiento cuando se reproduce.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**administrador de animaciones** 
</dt> <dd>

Componente principal de Windows animación y la interfaz de programación central para administrar (crear, programar y controlar) animaciones.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**temporizador de animación**
</dt> <dd>

Componente para proporcionar servicios de control de tiempo que se pueden usar junto con el administrador de animaciones. Limita dinámicamente la velocidad de fotogramas en función de la carga de la aplicación y del sistema o en modo de bajo consumo. Consulte también: limitación.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variable de animación** 
</dt> <dd>

Valor que se puede animar. Las variables de animación se pueden usar para representar la posición, el tamaño, la rotación, la transparencia y otras calidades de los objetos visibles.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Cancelación**
</dt> <dd>

Proceso de eliminación de un guión gráfico de la programación antes de que haya empezado a reproducirse.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**Compresión**
</dt> <dd>

Un desforme de la percepción de tiempo de un guión gráfico. El sistema aumenta la velocidad a la que progresa el guión gráfico pasando valores de tiempo de entrada que aumentan más rápido que el reloj del sistema.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**Conclusión**
</dt> <dd>

El proceso de dirigir un guión gráfico para salir de los bucles indefinidos. Si el bucle ha comenzado, la iteración actual se completará y el resto del guión gráfico se reproducirá. De lo contrario, la parte en bucle del guión gráfico se omitirá por completo.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**marco** 
</dt> <dd>

Una sola imagen en una película o animación.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**velocidad de fotogramas** 
</dt> <dd>

Número de fotogramas mostrados por segundo. Un mayor número de fotogramas de vídeo normalmente genera un movimiento más suave en la imagen.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolador**
</dt> <dd>

Objeto de programación que realiza la interpolación matemática del valor y la velocidad de una variable para una transición.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Fotograma clave**
</dt> <dd>

Un momento en el tiempo dentro de un guión gráfico, que se puede especificar en relación con el inicio del guión gráfico, con respecto a otro fotograma clave, o al final de una transición, y se usa para especificar la hora de inicio y finalización de otras transiciones o un ciclo dentro del guión gráfico.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**Bucle**
</dt> <dd>

Sección de un guión gráfico entre dos fotogramas clave que se reproduce repetidamente. Un bucle puede reproducir un número finito de veces o indefinidamente.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparación de prioridad** 
</dt> <dd>

Código definido por el cliente que compara dos guiones gráficos, uno ya programado y otro a punto de programarse, para determinar su prioridad relativa. Un guión gráfico programado se puede recortar, comprimir, cancelar o concluir para habilitar la programación del guión gráfico con mayor prioridad.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**storyboard** 
</dt> <dd>

Un grupo de transiciones de animación sincronizadas entre sí.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**etiqueta** 
</dt> <dd>

Un par que consta de un identificador entero y un objeto COM usado por una aplicación para identificar variables de animación y guiones gráficos dentro del ámbito de un administrador de animación específico.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitación** 
</dt> <dd>

Ajuste dinámico de la velocidad de fotogramas de una animación para satisfacer determinados requisitos. La limitación ayuda a garantizar que las animaciones se representan a una velocidad de fotogramas coherente, al tiempo que minimiza el uso de recursos del sistema para la representación a una velocidad superior a la necesaria o útil.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**tick** 
</dt> <dd>

Evento de temporizador que normalmente desencadena la representación de un único fotograma.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transición** 
</dt> <dd>

Construcción que define actualizaciones progresivas para una variable de animación durante un período de tiempo.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**Recorte**
</dt> <dd>

Adelantar el control de un guión gráfico de una variable de animación con un guión gráfico de mayor prioridad. Si el recorte de un guión gráfico en una o varias variables hace que el guión gráfico finalice prematuramente, se considera truncado. Vea también: truncamiento.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**Truncamiento**
</dt> <dd>

Finalizar un guión gráfico prematuramente al adelantar el control de una o varias de las variables que anima con uno o varios guiones gráficos de mayor prioridad. Vea también: recorte.

</dd> </dl>

 

 




