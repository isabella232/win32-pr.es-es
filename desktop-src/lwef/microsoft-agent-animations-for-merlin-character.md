---
title: Animaciones de Microsoft Agent para el carácter Desándes
description: Animaciones de Microsoft Agent para el carácter Desándes
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797002897f0e3bdb7efb309de8b73a33df8bdf399279895be8daa2b47d8ec084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247478"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Animaciones de Microsoft Agent para el carácter Desándes

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El [carácter Descuido del agente](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) de Microsoft es un trabajo protegido por derechos de Microsoft Corporation.

Ya es compatible con las animaciones enumeradas en la tabla siguiente. Consulte [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) and Programming the Microsoft Agent Control (Programación de la interfaz del servidor de Microsoft Agent) y Programming the Microsoft Agent Control [(Programación](programming-the-microsoft-agent-control.md) del control de Agente de Microsoft) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor del control, tenga en cuenta cómo las descargará. En lugar de descargar todas las animaciones a la  vez, es posible que desee recuperar primero las animaciones de estado **Mostrando** y Hablando. Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se bajan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de caracteres y animaciones se cargan correctamente, use el [**evento RequestComplete.**](requestcomplete-event.md) Si se produce un error en una solicitud de carga, puede volver a cargar los datos o mostrar un mensaje adecuado.

Si la animación **Return** de una animación se define mediante ramas exit, no es necesario llamarla explícitamente; El Agente reproduce automáticamente la **animación Return** antes de la animación siguiente. Sin embargo, si **aparece una animación Return,** debe llamar a la animación mediante el método [**Play**](play-method.md) antes que otra animación para proporcionar una transición fluida. Si no **aparece ninguna** animación Return, la animación normalmente finaliza sin necesidad de una animación de transición.

El archivo de caracteres incluye efectos de sonido para algunas animaciones, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades de Microsoft Agent. También puede deshabilitar los efectos de sonido en la aplicación.



| Animación                 | Animación de devolución         | Admite habla | Efectos de sonido | Asignado al estado                            | Descripción                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Confirmación**           | Ninguno                     | No                | **No**        | None                                         | Cabeza de los nods                                        |
| **Alerta**                 | Sí, mediante ramas de salida | Sí               | **No**        | **Escuchar**                                | Se enderezan y elevan las indesaciones.                  |
| **Anunciar**              | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Provoca la insondía y las interpretaciones                         |
| **Blink**                 | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadea con los ojos                                      |
| **Confusión**              | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Rasca la cabeza                                   |
| **Felicitar**          | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Muestra el trofeo                                  |
| **\_Indulte 2**       | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Aplaude                                         |
| **Rechazar**               | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Eleva las manos y agite la cabeza                     |
| **DoMagic1**              | None                     | Sí               | **No**        | None                                         | Genera una vaguada mágica                                |
| **DoMagic2**              | Sí, mediante ramas de salida | No                | **Sí**       | None                                         | Varone inferior, aparecen nubes                       |
| **DontRecognize**         | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Se sujeta de la mano a la orejita                                |
| **Explicación**               | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Extiende los lados.                             |
| **GestureDown**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                    |
| **GestureLeft**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                    |
| **GestureRight**          | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                   |
| **GestureUp**             | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                      |
| **GetAttention**          | **GetAttentionReturn**   | Sí               | **Sí**       | None                                         | Se inclina hacia delante y se desenvía                         |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sí               | **Sí**       | None                                         | Inclinarse hacia delante, volver a desenlazar                    |
| **GetAttentionReturn**    | Ninguno                     | No                | **No**        | None                                         | Vuelve a la posición neutra                      |
| **Acogida**                 | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Arcos                                             |
| **Audiencia \_ 1**            | Ninguno                     | No                | **No**        | **Oído**                                  | Extensión de las ruedas \* (animación de bucle)                |
| **Audiencia \_ 2**            | Ninguno                     | No                | **No**        | **Oído**                                  | Inclina la cabeza izquierda \* (animación de bucle)            |
| **Audiencia \_ 3**            | Ninguno                     | No                | **No**        | **Oído**                                  | Gira la cabeza a la izquierda \* (animación de bucle)            |
| **Audiencia \_ 4**            | Ninguno                     | No                | **No**        | **Oído**                                  | Gira la cabeza a la derecha \* (animación de bucle)           |
| **Ocultar**                  | Ninguno                     | No                | **Sí**       | **Escondiendo**                                   | Desaparece bajo el límite                             |
| **Idle1 \_ 1**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Toma el aire                                     |
| **Idle1 \_ 2**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas a la izquierda y parpadeos                          |
| **Idle1 \_ 3**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | De un vistazo a la derecha                                    |
| **Idle1 \_ 4**              | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia la derecha y parpadeos               |
| **Idle2 \_ 1**              | Ninguno                     | No                | **No**        | **IdlingLevel2**                             | Examina wand y parpadea                         |
| **Idle2 \_ 2**              | Ninguno                     | No                | **No**        | **IdlingLevel2**                             | Manos y parpadeos                           |
| **Idle3 \_ 1**              | Ninguno                     | No                | **Sí**       | **IdlingLevel3**                             | Bostezos                                            |
| **Idle3 \_ 2**              | Sí, mediante ramas de salida | No                | **Sí**       | **IdlingLevel3**                             | Se queda sin vida \* (animación de bucle)               |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | None                                         | Busca hacia abajo.                                       |
| **LookDownBlink**         | **LookDownReturn**       | No                | **No**        | None                                         | Parpadeos mirando hacia abajo                              |
| **LookDownReturn**        | Ninguno                     | No                | **No**        | None                                         | Vuelve a la posición neutra                      |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | None                                         | Se ve a la izquierda                                       |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **No**        | None                                         | Parpadeos que miran a la izquierda                              |
| **LookLeftReturn**        | Ninguno                     | No                | **No**        | None                                         | Vuelve a la posición neutra                      |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | None                                         | Parece correcto                                      |
| **LookRightBlink**        | **LookRightReturn**      | No                | **No**        | None                                         | Parpadeos que miran a la derecha                             |
| **LookRightReturn**       | Ninguno                     | No                | **No**        | None                                         | Vuelve a la posición neutra                      |
| **Búsqueda**                | **LookUpReturn**         | No                | **No**        | None                                         | Busca                                         |
| **LookUpBlink**           | **LookUpReturn**         | No                | **No**        | None                                         | Parpadeos al buscar                                |
| **LookUpReturn**          | Ninguno                     | No                | **No**        | None                                         | Vuelve a la posición neutra                      |
| **MoveDown**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingDown**                               | Abalo desa,                                       |
| **MoveLeft**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingLeft**                               | A la izquierda                                       |
| **MoveRight**             | Sí, mediante ramas de salida | No                | **Sí**       | **MovingRight**                              | Derecho de las derechas                                      |
| **MoveUp**                | Sí, mediante ramas de salida | No                | **Sí**       | **MovingUp**                                 | A la intesa                                         |
| **complacido**               | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Sonriente y se mantiene de la mano                  |
| **Process**               | No                       | No                | **Sí**       | None                                         | Caldron Desastros                                    |
| **Procesamiento**            | Sí, mediante ramas de salida | No                | **Sí**       | None                                         | Caldron Desastroso \* (animación de bucle)              |
| **Lectura**                  | **ReadReturn**           | Sí               | **Sí**       | None                                         | Abre el libro, lee y busca                   |
| **ReadContinued**         | **ReadReturn**           | Sí               | **Sí**       | None                                         | Lee y busca                               |
| **ReadReturn**            | Ninguno                     | No                | **Sí**       | None                                         | Vuelve a la posición neutra                      |
| **Lectura**               | Sí, mediante ramas de salida | No                | **Sí**       | None                                         | Lecturas \* (animación de bucle)                      |
| **RestPose**              | None                     | Sí               | **No**        | **Hablando**                                 | Posición neutra                                 |
| **Triste**                   | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Expresión desafortunada                                   |
| **Búsqueda**                | No                       | No                | **Sí**       | None                                         | Busca en la bola de cristal                          |
| **Buscando**             | Sí, mediante ramas de salida | No                | **Sí**       | None                                         | Busca en la bola de cristal \* (animación de bucle)    |
| **Mostrar**                  | Ninguno                     | No                | **Sí**       | **Mostrando**                                  | Aparece sin límite                               |
| **StartListening**        | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Coloca la mano al oído                                 |
| **StopListening**         | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Coloca las manos sobre las manos                             |
| **Sugerir**               | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Muestra bombilla                               |
| **Sorprendido**             | Sí, mediante ramas de salida | Sí               | **Sí**       | None                                         | Parece que se ha quedo con la                                  |
| **Pensar**                 | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Busca con la mano en la chin                       |
| **Pensando**              | No                       | No                | **No**        | None                                         | Busca con la mano en la chin (animación \* de bucle) |
| **Incierto**             | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Se inclina hacia delante y aumenta el desenlace.                 |
| **Onda**                  | Sí, mediante ramas de salida | Sí               | **No**        | None                                         | Olas                                            |
| **Escritura**                 | **WriteReturn**          | Sí               | **Sí**       | None                                         | Abre el libro, escribe y busca                  |
| **WriteContinued**        | **WriteReturn**          | Sí               | **Sí**       | None                                         | Escribe y busca                              |
| **WriteReturn**           | Ninguno                     | No                | **Sí**       | None                                         | Vuelve a la posición neutra                      |
| **Escritura**               | Sí, mediante ramas de salida | No                | **Sí**       | None                                         | Escrituras \* (animación de bucle)                     |



 

\* Si reproduce una animación en bucle, debe usar [**Detener**](stop-method.md) para borrarla antes de que se reprodguen otras animaciones de la cola del carácter.

 

