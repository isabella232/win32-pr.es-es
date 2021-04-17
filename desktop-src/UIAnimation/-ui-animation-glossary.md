---
title: Glosario de animaciones de Windows
description: Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan el administrador de animaciones de Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animación de Windows animación de Windows, Glosario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "104532943"
---
# <a name="windows-animation-glossary"></a>Glosario de animaciones de Windows

Este glosario contiene términos y acrónimos de interés para los desarrolladores que usan el administrador de animaciones de Windows.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animación** de 
</dt> <dd>

Secuencia de imágenes sintéticas y consecutivas que produce una ilusión de movimiento cuando se reproduce.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Administrador de animaciones** 
</dt> <dd>

Componente básico de la animación de Windows y la interfaz de programación central para administrar (crear, programar y controlar) animaciones.

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**temporizador de animación**
</dt> <dd>

Componente que proporciona servicios de control de tiempo que se pueden usar junto con el administrador de animaciones. Limita dinámicamente la velocidad de fotogramas en función de la carga de la aplicación y del sistema o en el modo de baja energía. Vea también: limitación.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variable de animación** 
</dt> <dd>

Valor que se puede animar. Las variables de animación se pueden usar para representar la posición, el tamaño, la rotación, la transparencia y otras cualidades de los objetos visibles.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**cancelación**
</dt> <dd>

El proceso de quitar un guion gráfico de la programación antes de empezar a reproducir.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**presi**
</dt> <dd>

Deformación de la percepción de tiempo de un guion gráfico. El sistema aumenta la velocidad a la que progresa el guión gráfico pasando los valores de tiempo de entrada que aumentan más rápido que el reloj del sistema.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**celebre**
</dt> <dd>

Proceso de dirigir un guion gráfico para salir de los bucles indefinidos. Si el bucle se ha iniciado, la iteración actual se completará y, a continuación, se reproducirá el resto del guión gráfico. De lo contrario, la parte en bucle del guión gráfico se omitirá por completo.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**marco** de 
</dt> <dd>

Una sola imagen en una película o una animación.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**velocidad de fotogramas** 
</dt> <dd>

Número de fotogramas mostrados por segundo. Un mayor número de fotogramas de vídeo normalmente genera un movimiento más suave en la imagen.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolador**
</dt> <dd>

Objeto de programación que realiza la interpolación matemática del valor y la velocidad de una variable para una transición.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**fotograma clave**
</dt> <dd>

Un momento en el tiempo dentro de un guion gráfico, que se puede especificar en relación con el inicio del guion gráfico, con respecto a otro fotograma clave o en el momento de finalización de una transición y que se usa para especificar la hora de inicio y de finalización de otras transiciones o un ciclo dentro del guión gráfico.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**realizar**
</dt> <dd>

Sección de un guión gráfico entre dos fotogramas clave que se reproduce repetidamente. Un bucle puede reproducirse un número finito de veces o indefinidamente.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparación de prioridad** 
</dt> <dd>

Código definido por el cliente que compara dos guiones gráficos, uno ya programado y el otro sobre el que se va a programar, para determinar su prioridad relativa. Un guión gráfico programado se puede recortar, comprimir, cancelar o concluir para habilitar la programación del guion gráfico con mayor prioridad.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**guión gráfico** 
</dt> <dd>

Grupo de transiciones de animación sincronizadas entre sí.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**etiqueta** de 
</dt> <dd>

Par formado por un identificador entero y un objeto COM que usa una aplicación para identificar las variables de animación y los guiones gráficos en el ámbito de un administrador de animaciones específico.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitación** 
</dt> <dd>

Ajuste dinámico de la velocidad de fotogramas de una animación para cumplir determinados requisitos. La limitación ayuda a garantizar que las animaciones se representen a una velocidad de fotogramas coherente a la vez que se minimiza el uso de los recursos del sistema para la representación a una velocidad superior a la que se necesita o es útil.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**marca** 
</dt> <dd>

Un evento de temporizador que normalmente desencadena la representación de un solo fotograma.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transición** 
</dt> <dd>

Una construcción que define las actualizaciones progresivas para una variable de animación a lo largo de un período de tiempo.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**desechos**
</dt> <dd>

Adelantar el control de un guión gráfico de una variable de animación con un guión gráfico de mayor prioridad. Si el recorte de un guion gráfico en una o varias variables hace que el guión gráfico finalice prematuramente, se considerará truncado. Vea también: truncamiento.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**truncamiento**
</dt> <dd>

Finalización prematura de un guión gráfico mediante el control de una o varias de las variables que anima con uno o más guiones gráficos de mayor prioridad. Vea también: recorte.

</dd> </dl>

 

 




