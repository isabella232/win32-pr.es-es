---
title: Animaciones de Microsoft Agent para el carácter Genie
description: Animaciones de Microsoft Agent para el carácter Genie
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204da244b74e96e239d540662dabf73af82001748b395da8e660f53fe4cf85e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976105"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Animaciones de Microsoft Agent para el carácter Genie

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Microsoft [Agent Genie Character es](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) un trabajo protegido por derechos de autor de Microsoft Corporation.

Genie admite las animaciones enumeradas en la tabla siguiente. Consulte Programming the Microsoft Agent Server Interface (Programación de la interfaz del servidor de [Microsoft Agent)](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) y [Programming the Microsoft Agent Control (Programación](programming-the-microsoft-agent-control.md) del control de agente de Microsoft) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método [**Get**](get-method.md) o [**prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor del control, considere cómo las descargará. En lugar de descargar todas las animaciones a  la vez, puede que desee recuperar primero las animaciones de estado **Mostrando** y Hablando. Esto le permitirá mostrar el carácter rápidamente y hacer que se diga mientras se desanan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de caracteres y animaciones se cargan correctamente, use el [**evento RequestComplete.**](requestcomplete-event.md) Si se produce un error en una solicitud de carga, puede volver a cargar los datos o mostrar un mensaje adecuado.

Si las animaciones **Return** de una animación se definen mediante ramas exit, no es necesario llamarla explícitamente; El Agente reproduce automáticamente la **animación Devolución** antes de la animación siguiente. Sin embargo, si aparece **una animación Return,** debe llamar a la animación mediante el método [**Play**](play-method.md) antes de otra animación para proporcionar una transición sin problemas. Si no **aparece ninguna** animación Return, la animación normalmente finaliza sin necesidad de una animación de transición.

El archivo de caracteres incluye efectos de sonido para alguna animación, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades de Microsoft Agent. También puede deshabilitar los efectos de sonido en la aplicación.



| Animación                 | Animación de devolución         | Admite habla | Efectos de sonido | Asignado al estado                            | Descripción                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Confirmación**           | Ninguno                     | No                | **No**        | Ninguno                                         | Cabeza de nods                                                      |
| **Alerta**                 | Sí, mediante ramas de salida | Sí               | **No**        | **Escuchar**                                | Endereza y aumenta las iniciones.                                |
| **Anunciar**              | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Eleva la mano                                                    |
| **Blink**                 | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadea los ojos                                                    |
| **Confusión**              | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Cabeza de scratches                                                 |
| **Felicitar**          | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Aplaude                                                       |
| **\_Indulte 2**       | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Gesto de subir el control de posición                                        |
| **Rechazar**               | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Eleva las manos y agite la cabeza                                   |
| **DoMagic1**              | Ninguno                     | Sí               | **No**        | Ninguno                                         | Se gira a un lado y se elevan las manos                                 |
| **DoMagic2**              | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Se reducen las manos, aparecen nubes                                    |
| **No reconoce**         | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Mano a oído                                              |
| **Explicación**               | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Extiende los brazos al lado                                           |
| **GestureDown**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                                  |
| **GestureLeft**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                                  |
| **GestureRight**          | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                                 |
| **GestureUp**             | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Sí               | **No**        | Ninguno                                         | Ondas de las manos                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sí               | **No**        | Ninguno                                         | Ondas de nuevo                                               |
| **GetAttentionReturn**    | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **Acogida**                 | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Arcos                                                           |
| **Audiencia \_ 1**            | Ninguno                     | No                | **No**        | **Oído**                                  | Extensión de las ruedas \* (animación de bucle)                              |
| **Audiencia \_ 2**            | Ninguno                     | No                | **No**        | **Oído**                                  | Inclina la cabeza izquierda \* (animación de bucle)                          |
| **Audiencia \_ 3**            | Ninguno                     | No                | **No**        | **Oído**                                  | Gira la cabeza a la izquierda \* (animación de bucle)                          |
| **Audiencia \_ 4**            | Ninguno                     | No                | **No**        | **Oído**                                  | Gira la cabeza a la derecha \* (animación de bucle)                         |
| **Ocultar**                  | Ninguno                     | No                | **Sí**       | **Escondiendo**                                   | Desaparece en el humo                                          |
| **Idle1 \_ 1**              | Ninguno                     | No                | **No**        | **IdlingLevel1** IdlingLevel2                | Toma el resa,                                                   |
| **Idle1 \_ 2**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas a la derecha y parpadeos                                       |
| **Idle1 \_ 3**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas a la izquierda y parpadeos                                        |
| **Idle1 \_ 4**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia la derecha y parpadeos                             |
| **Idle1 \_ 5**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia abajo y parpadeos                                        |
| **Idle1 \_ 6**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia arriba y parpadeos                                          |
| **Idle2 \_ 1**              | Ninguno                     | No                | **No**        | **IdlingLevel2**                             | Wisp y wisp                                                    |
| **Idle2 \_ 2**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel2**                             | Muestra el desplazamiento y las lecturas                                       |
| **Idle2 \_ 3**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel2**                             | Revela el desplazamiento y las escrituras                                      |
| **Idle3 \_ 1**              | Ninguno                     | No                | **Sí**       | **IdlingLevel3**                             | Bostezos                                                          |
| **Idle3 \_ 2**              | Sí, mediante ramas de salida | No                | **Sí**       | **IdlingLevel3**                             | Se queda sin vida \* (animación de bucle)                             |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | Ninguno                                         | Busca hacia abajo.                                                     |
| **LookDownBlink**         | **LookDownReturn**       | No                | **No**        | Ninguno                                         | Parpadeos mirando hacia abajo                                            |
| **LookDownReturn**        | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | Ninguno                                         | Se ve a la izquierda                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **No**        | Ninguno                                         | Parpadeos que miran a la izquierda                                            |
| **LookLeftReturn**        | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | Ninguno                                         | Parece correcto                                                    |
| **LookRightBlink**        | **LookRightReturn**      | No                | **No**        | Ninguno                                         | Parpadeos que miran a la derecha                                           |
| **LookRightReturn**       | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **Búsqueda**                | **LookUpReturn**         | No                | **No**        | Ninguno                                         | Busca                                                       |
| **LookUpBlink**           | **LookUpReturn**         | No                | **No**        | Ninguno                                         | Parpadeos al buscar                                              |
| **LookUpReturn**          | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **MoveDown**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingDown**                               | Abalo desa,                                                     |
| **MoveLeft**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingLeft**                               | A la izquierda                                                     |
| **MoveRight**             | Sí, mediante ramas de salida | No                | **Sí**       | **MovingRight**                              | Derecho de las derechas                                                    |
| **MoveUp**                | Sí, mediante ramas de salida | No                | **Sí**       | **MovingUp**                                 | A la intesa                                                       |
| **complacido**               | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Sonriente y se mantiene de la mano                                |
| **Process**               | No                       | No                | **No**        | Ninguno                                         | Gira en una nube                                             |
| **Procesamiento**            | Sí, mediante ramas de salida | No                | **No**        | Ninguno                                         | Gira en una nube (animación \* de bucle)                       |
| **Lectura**                  | **ReadReturn**           | Sí               | **Sí**       | Ninguno                                         | Muestra el desplazamiento, las lecturas y las miradas                             |
| **ReadContinued**         | **ReadReturn**           | Sí               | **No**        | Ninguno                                         | Lee y busca                                             |
| **ReadReturn**            | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **Lectura**               | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Mostrar desplazamiento y lecturas \* (animación de bucle)                  |
| **RestPose**              | Ninguno                     | Sí               | **No**        | **Hablando**                                 | Posición neutra                                               |
| **Triste**                   | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Expresión desafortunada                                                 |
| **Búsqueda**                | No                       | No                | **No**        | Ninguno                                         | Revela binoculares y turnos                                   |
| **Buscando**             | Sí, mediante ramas de salida | No                | **No**        | Ninguno                                         | Revela los binoculares y los turnos (animación \* en bucle)             |
| **Mostrar**                  | Ninguno                     | No                | **Sí**       | **Mostrando**                                  | Aparece sin humo                                           |
| **StartListening**        | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Coloca la mano al oído                                               |
| **StopListening**         | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Coloca las manos sobre las manos.                                           |
| **Sugerir**               | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Muestra bombilla                                             |
| **Sorprendido**             | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Parece ser una sorpresa                                                |
| **Pensar**                 | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Busca con la mano en la chin.                                     |
| **Pensando**              | No                       | No                | **No**        | Ninguno                                         | Busca con la mano en la chin (animación \* en bucle)               |
| **Incierto**             | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Mueve una mano a la chin, otra a la altura y eleva la mano derecha. |
| **Onda**                  | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Olas                                                          |
| **Escritura**                 | **WriteReturn**          | Sí               | **Sí**       | Ninguno                                         | Muestra el desplazamiento, escribe y busca                            |
| **WriteContinued**        | **WriteReturn**          | Sí               | **Sí**       | Ninguno                                         | Escribe y busca                                            |
| **WriteReturn**           | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                    |
| **Escritura**               | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Muestra el desplazamiento, las escrituras \* (animación en bucle)                   |



 

\* Si reproduce una animación en bucle, debe usar [**Detener**](stop-method.md) para borrarla antes de que se reprodguen otras animaciones en la cola del carácter.

 

