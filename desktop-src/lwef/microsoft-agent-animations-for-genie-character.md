---
title: Animaciones del agente de Microsoft para el carácter de genio
description: Animaciones del agente de Microsoft para el carácter de genio
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f583fc6540b5fe13cc157542d69352a8ea5b31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420712"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Animaciones del agente de Microsoft para el carácter de genio

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El [personaje de Microsoft Agent genio](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) es un trabajo con copyright de Microsoft Corporation.

Genio admite las animaciones que se muestran en la tabla siguiente. Consulte [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) and [Programming the Microsoft Agent control](programming-the-microsoft-agent-control.md) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor [**Get**](get-method.md) o del servidor, tenga en cuenta cómo se descargarán. En lugar de descargar todas las animaciones a la vez, puede que desee recuperar primero las animaciones de estado de **visualización** y de **habla** . Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se desconectan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de animación y de caracteres se cargan correctamente, use el evento [**RequestComplete**](requestcomplete-event.md) . Si se produce un error en una solicitud de carga, puede volver a intentar cargar los datos o mostrar un mensaje adecuado.

Si las animaciones **devueltas** de una animación se definen mediante ramas de salida, no es necesario llamarlas explícitamente. El agente reproduce automáticamente la animación **devuelta** antes de la siguiente animación. Sin embargo, si se muestra una animación de **devolución** , debe llamar a la animación con el método [**Play**](play-method.md) antes de otra animación para proporcionar una transición suave. Si no aparece ninguna animación **devuelta** , la animación finaliza normalmente sin necesidad de una animación transitoria.

El archivo de caracteres incluye efectos sonoros en algunas animaciones, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades del agente de Microsoft. También puede deshabilitar los efectos sonoros en la aplicación.



| Animación                 | Devolver animación         | Admite hablar | Efectos sonoros | Asignado a estado                            | Descripción                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Confirmación**           | None                     | No                | **No**        | None                                         | Encabezado nodos                                                      |
| **Alerta**                 | Sí, usar ramas de salida | Sí               | **No**        | **Escucha**                                | Activa y produce eyebrows                                |
| **Anuncie**              | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Levanta la mano                                                    |
| **Blink**                 | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadeos                                                    |
| **Confusión**              | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Cabeza de arañazos                                                 |
| **Felicitar**          | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Applauds                                                       |
| **Felicitación \_ 2**       | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Permite el movimiento de pulgas                                        |
| **Rechazar**               | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Lanza manos y sacudidas                                   |
| **DoMagic1**              | None                     | Sí               | **No**        | None                                         | Se convierte en el lado y se lanza manos                                 |
| **DoMagic2**              | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Bajar las manos, aparecen las nubes                                    |
| **DontRecognize**         | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Incluye mano a las lengüetas                                              |
| **Explicación**               | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Extiende los brazos al lado                                           |
| **GestureDown**           | Sí, usar ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                                  |
| **GestureLeft**           | Sí, usar ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                                  |
| **GestureRight**          | Sí, usar ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                                 |
| **GestureUp**             | Sí, usar ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Sí               | **No**        | None                                         | Ramas de olas                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sí               | **No**        | None                                         | Ramas de nuevo                                               |
| **GetAttentionReturn**    | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **Acogida**                 | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Bow                                                           |
| **Audición \_ 1**            | None                     | No                | **No**        | **Oído**                                  | Extender los oídos ( \* animación en bucle)                              |
| **Audición \_ 2**            | None                     | No                | **No**        | **Oído**                                  | Inclina la izquierda ( \* animación en bucle)                          |
| **Audición \_ 3**            | None                     | No                | **No**        | **Oído**                                  | Desactiva la cabeza ( \* animación en bucle)                          |
| **Audición \_ 4**            | None                     | No                | **No**        | **Oído**                                  | Convierte la punta a la derecha ( \* animación de bucle)                         |
| **Ocultar**                  | None                     | No                | **Sí**       | **Conde**                                   | Desaparece en humo                                          |
| **Idle1 \_ 1**              | None                     | No                | **No**        | **IdlingLevel1** IdlingLevel2                | Toma respiración                                                   |
| **Idle1 \_ 2**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Mirada a la derecha y a los parpadeos                                       |
| **Idle1 \_ 3**              | Sí, usar ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Mirar a la izquierda y a los parpadeos                                        |
| **Idle1 \_ 4**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Un vistazo a la derecha y los parpadeos                             |
| **Idle1 \_ 5**              | Sí, usar ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vista rápida y parpadeo                                        |
| **Idle1 \_ 6**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | El vistazo y los parpadeos                                          |
| **Idle2 \_ 1**              | None                     | No                | **No**        | **IdlingLevel2**                             | Serpientes WISP                                                    |
| **Idle2 \_ 2**              | Sí, usar ramas de salida | No                | **No**        | **IdlingLevel2**                             | Revela desplazamientos y lecturas                                       |
| **Idle2 \_ 3**              | Sí, usar ramas de salida | No                | **No**        | **IdlingLevel2**                             | Revela desplazamientos y escrituras                                      |
| **Idle3 \_ 1**              | None                     | No                | **Sí**       | **IdlingLevel3**                             | Yawns                                                          |
| **Idle3 \_ 2**              | Sí, usar ramas de salida | No                | **Sí**       | **IdlingLevel3**                             | Está en suspensión ( \* animación en bucle)                             |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | None                                         | Buscar                                                     |
| **LookDownBlink**         | **LookDownReturn**       | No                | **No**        | None                                         | Parpadea al mirar                                            |
| **LookDownReturn**        | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | None                                         | Aparece a la izquierda                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **No**        | None                                         | Parpadea al mirar a la izquierda                                            |
| **LookLeftReturn**        | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | None                                         | Parece correcto                                                    |
| **LookRightBlink**        | **LookRightReturn**      | No                | **No**        | None                                         | Parpadea al mirar a la derecha                                           |
| **LookRightReturn**       | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **Buscar**                | **LookUpReturn**         | No                | **No**        | None                                         | Busca                                                       |
| **LookUpBlink**           | **LookUpReturn**         | No                | **No**        | None                                         | Parpadeo de búsqueda                                              |
| **LookUpReturn**          | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **Bajar**              | Sí, usar ramas de salida | No                | **Sí**       | **MovingDown**                               | Volar                                                     |
| **MoveLeft**              | Sí, usar ramas de salida | No                | **Sí**       | **MovingLeft**                               | Volar a la izquierda                                                     |
| **Anula**             | Sí, usar ramas de salida | No                | **Sí**       | **MovingRight**                              | Volar a la derecha                                                    |
| **MoveUp**                | Sí, usar ramas de salida | No                | **Sí**       | **MovingUp**                                 | Volar                                                       |
| **Satisfechos**               | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Sonrisas y mantiene las manos juntas                                |
| **Proceso**               | No                       | No                | **No**        | None                                         | Gira en una nube                                             |
| **Processing**            | Sí, usar ramas de salida | No                | **No**        | None                                         | Gira en una nube ( \* animación en bucle)                       |
| **Lectura**                  | **ReadReturn**           | Sí               | **Sí**       | None                                         | Revela desplazarse, leer y buscar                             |
| **ReadContinued**         | **ReadReturn**           | Sí               | **No**        | None                                         | Lee y busca                                             |
| **ReadReturn**            | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **Leía**               | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Mostrar desplazamiento y lecturas ( \* animación en bucle)                  |
| **RestPose**              | None                     | Sí               | **No**        | **Habla**                                 | Posición neutra                                               |
| **San**                   | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Sad (expresión)                                                 |
| **Búsqueda**                | No                       | No                | **No**        | None                                         | Revela prismáticos y vueltas                                   |
| **Buscándol**             | Sí, usar ramas de salida | No                | **No**        | None                                         | Revela prismáticos y vueltas ( \* animación en bucle)             |
| **Mostrar**                  | None                     | No                | **Sí**       | **Mostrando**                                  | Aparece fuera del humo                                           |
| **StartListening**        | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Coloca la mano en el oído                                               |
| **StopListening**         | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Pone a mano los oídos                                           |
| **Sugerir**               | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Muestra bombilla                                             |
| **Sorprendido**             | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Aspecto sorprendido                                                |
| **Opina**                 | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Busca de forma manual en el mentón                                     |
| **Pensando**              | No                       | No                | **No**        | None                                         | Busca en el mentón ( \* animación en bucle)               |
| **Seguro**             | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Mueve una mano a Chin, de otro a hip, y eleva el eyebrow derecho |
| **Ondas**                  | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Ondas                                                          |
| **Escritura**                 | **WriteReturn**          | Sí               | **Sí**       | None                                         | Revela desplazarse, escribir y buscar                            |
| **WriteContinued**        | **WriteReturn**          | Sí               | **Sí**       | None                                         | Escribe y busca                                            |
| **WriteReturn**           | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                    |
| **Escribir**               | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Revela desplazamiento, escrituras ( \* animación en bucle)                   |



 

\* Si reproduce una animación de bucle, debe utilizar [**detener**](stop-method.md) para borrarla antes de que se reproduzcan otras animaciones en la cola del carácter.

 

