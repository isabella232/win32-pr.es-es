---
title: Animaciones de Microsoft Agent para el carácter despiadado
description: Animaciones de Microsoft Agent para el carácter despiadado
ms.assetid: 335d915c-9cae-4850-a6bf-66ad78d533ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46682d8836fc02a8d19d5b40e8fddef4068a1d14190c2919042ff1087a745acb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888115"
---
# <a name="microsoft-agent-animations-for-peedy-character"></a>Animaciones de Microsoft Agent para el carácter despiadado

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Microsoft [Agent Captiondy Character es](https://www.microsoft.com/downloads/details.aspx?FamilyID=bd3c4655-79e4-4791-ab9d-abc7bbd133ef) un trabajo protegido por derechos de Microsoft Corporation.

Dy admite las animaciones enumeradas en la tabla siguiente. Consulte [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) and Programming the Microsoft Agent Control (Programación de la interfaz del servidor de Microsoft Agent) y Programming the Microsoft Agent Control [(Programación](programming-the-microsoft-agent-control.md) del control de Agente de Microsoft) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor del control, tenga en cuenta cómo las descargará. En lugar de descargar todas las animaciones a la  vez, puede que desee recuperar primero las animaciones de estado **Mostrando** y Hablando. Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se bajan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de caracteres y animaciones se cargan correctamente, use el [**evento RequestComplete.**](requestcomplete-event.md) Si se produce un error en una solicitud de carga, puede volver a cargar los datos o mostrar un mensaje adecuado.

Si la animación **Return** de una animación se define mediante ramas exit, no es necesario llamarla explícitamente; El Agente reproduce automáticamente la **animación Return** antes de la siguiente animación. Sin embargo, si **aparece una animación Return,** debe llamar a la animación mediante el método [**Play**](play-method.md) antes que otra animación para proporcionar una transición fluida. Si no **aparece ninguna** animación Return, la animación normalmente finaliza sin necesidad de una animación de transición.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor del control, tenga en cuenta cómo las descargará. En lugar de descargar todas las animaciones a la  vez, puede que desee recuperar primero las animaciones de estado **Mostrando** y Hablando. Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se bajan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de caracteres y animaciones se cargan correctamente, use el [**evento RequestComplete.**](requestcomplete-event.md) Si se produce un error en una solicitud de carga, puede volver a cargar los datos o mostrar un mensaje adecuado.

El archivo de caracteres incluye efectos de sonido para algunas animaciones, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades de Microsoft Agent. También puede deshabilitar los efectos de sonido en la aplicación.



| Animación                  | Animación de devolución         | Admite habla | Efectos de sonido | Asignado al estado                            | Descripción                                            |
|----------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------------|
| **Confirmación**            | Ninguno                     | No                | **No**        | Ninguno                                         | Cabeza de los nods                                              |
| **Alerta**                  | Sí, mediante ramas de salida | Sí               | **No**        | **Escuchar**                                | Se enderezan y se elevan las indesaciones.                        |
| **Anunciar**               | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | El avión de papel entra y se desenvuelta                    |
| **Blink**                  | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadea con los ojos                                            |
| **Confusión**               | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Los ojos giran alrededor                                       |
| **Felicitar**           | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Muestra la cinta de opciones azul                                   |
| **Rechazar**                | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Agite la cabeza                                            |
| **DoMagic1**               | Ninguno                     | Sí               | **Sí**       | Ninguno                                         | Genera una vaguada mágica                                      |
| **DoMagic2**               | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Vanos inferiores, aparecen nubes                             |
| **DontRecognize**          | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Agite la cabeza y mantiene el ala al oído                      |
| **Explicación**                | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Extiende los lados.                                   |
| **GestureDown**            | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                          |
| **GestureLeft**            | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                          |
| **GestureRight**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                         |
| **GestureUp**              | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                            |
| **GetAttention**           | **GetAttentionReturn**   | Sí               | **Sí**       | Ninguno                                         | Salta con las alerones extendidas                       |
| **GetAttentionContinued**  | **GetAttentionReturn**   | Sí               | **Sí**       | Ninguno                                         | Salta de nuevo con las alitas extendidas.                 |
| **GetAttentionReturn**     | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **Acogida**                  | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Arcos                                                   |
| **Audiencia \_ 1**             | Ninguno                     | No                | **No**        | **Oído**                                  | Inclina la derecha de la cabeza \* (animación de bucle)                 |
| **Audiencia \_ 2**             | Ninguno                     | No                | **No**        | **Oído**                                  | Inclina la cabeza izquierda \* (animación de bucle)                  |
| **Audiencia \_ 3**             | Ninguno                     | No                | **No**        | **Oído**                                  | Gira la cabeza a la derecha y a la izquierda \* (animación de bucle)       |
| **Ocultar**                   | Ninguno                     | No                | **Sí**       | **Escondiendo**                                   | Desvía                                             |
| **Idle1 \_ 1**               | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Toma el aire                                           |
| **Idle1 \_ 2**               | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas a la derecha y parpadeos                               |
| **Idle1 \_ 3**               | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas a la izquierda y parpadeos                                |
| **Idle1 \_ 4**               | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia arriba y parpadeos                                  |
| **Idle1 \_ 5**               | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia abajo y parpadeos                                |
| **Idle2 \_ 1**               | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel2**                             | Se pone gafas de sol                                     |
| **Idle2 \_ 2**               | Ninguno                     | No                | **Sí**       | **IdlingLevel2**                             | Come un cracker                                         |
| **Idle3 \_ 1**               | Ninguno                     | No                | **Sí**       | **IdlingLevel3**                             | Bostezos                                                  |
| **Idle3 \_ 2**               | Sí, mediante ramas de salida | No                | **Sí**       | **IdlingLevel3**                             | Se queda sin vida \* (animación de bucle)                     |
| **Idle3 \_ 3**               | Sí, mediante ramas de salida | No                | **No**        | **IdlingLevel3**                             | Escucha música (animación \* de bucle)                 |
| **LookDownLookDownReturn** |                          | No                | **No**        | Ninguno                                         | Busca hacia abajo.                                             |
| **LookDownBlink**          | **LookDownReturn**       | No                | **Sí**       | Ninguno                                         | Parpadeos mirando hacia abajo                                    |
| **LookDownReturn**         | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **LookDownLeft**           | **LookDownLeftReturn**   | No                | **No**        | Ninguno                                         | Mira hacia abajo a la izquierda                                        |
| **LookDownLeftBlink**      | **LookDownLeftReturn**   | No                | **Sí**       | Ninguno                                         | Parpadeos hacia abajo a la izquierda                               |
| **LookDownLeftReturn**     | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **LookDownRight**          | **LookDownRightReturn**  | No                | **No**        | Ninguno                                         | Mira hacia abajo a la derecha                                       |
| **LookDownRightBlink**     | **LookDownRightReturn**  | No                | **Sí**       | Ninguno                                         | Parpadea hacia abajo a la derecha                              |
| **LookDownRightReturn**    | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **LookLeft**               | **LookLeftReturn**       | Sí               | **No**        | Ninguno                                         | Se ve a la izquierda                                             |
| **LookLeftBlink**          | **LookLeftReturn**       | Sí               | **Sí**       | Ninguno                                         | Parpadeos que miran a la izquierda                                    |
| **LookLeftReturn**         | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **LookRight**              | **LookRightReturn**      | Sí               | **No**        | Ninguno                                         | Parece correcto                                            |
| **LookRightBlink**         | **LookRightReturn**      | Sí               | **Sí**       | Ninguno                                         | Parpadeos que miran a la derecha                                   |
| **LookRightReturn**        | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **Búsqueda**                 | **LookUpReturn**         | No                | **No**        | Ninguno                                         | Busca                                               |
| **LookUpBlink**            | **LookUpReturn**         | No                | **Sí**       | Ninguno                                         | Parpadeos al buscar                                      |
| **LookUpReturn**           | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **LookUpLeft**             | **LookUpLeftReturn**     | No                | **No**        | Ninguno                                         | Busca a la izquierda                                          |
| **LookUpLeftBlink**        | **LookUpLeftReturn**     | No                | **Sí**       | Ninguno                                         | Parpadeos hacia la izquierda                                 |
| **LookUpLeftReturn**       | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **LookUpRight**            | **LookUpRightReturn**    | No                | **No**        | Ninguno                                         | Busca a la derecha                                         |
| **LookUpRightBlink**       | **LookUpRightReturn**    | No                | **Sí**       | Ninguno                                         | Parpadeos que buscan a la derecha                                |
| **LookUpRightReturn**      | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **MoveDown**               | Sí, mediante ramas de salida | No                | **Sí**       | **MovingDown**                               | Abalo desa,                                             |
| **MoveLeft**               | Sí, mediante ramas de salida | No                | **Sí**       | **MovingLeft**                               | A la izquierda                                             |
| **MoveRight**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingRight**                              | Derecho de las derechas                                            |
| **MoveUp**                 | Sí, mediante ramas de salida | No                | **Sí**       | **MovingUp**                                 | A la intesa                                               |
| **complacido**                | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Sonrisas                                                 |
| **Process**                | Ninguno                     | No                | **Sí**       | Ninguno                                         | Usa la calculadora                                        |
| **Procesamiento**             | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Usa la calculadora \* (animación de bucle)                  |
| **Lectura**                   | **ReadReturn**           | Sí               | **Sí**       | Ninguno                                         | Abre una revista, lee y busca                     |
| **ReadContinued**          | **ReadReturn**           | Sí               | **Sí**       | Ninguno                                         | Lee y busca                                     |
| **ReadReturn**             | Ninguno                     | No                | **Sí**       | Ninguno                                         | Vuelve a la posición neutra                            |
| **Lectura**                | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Lecturas \* (animación de bucle)                            |
| **RestPose**               | Ninguno                     | Sí               | **No**        | **Hablando**                                 | Posición neutra                                       |
| **Triste**                    | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Expresión desafortunada                                         |
| **Búsqueda**                 | Ninguno                     | No                | **Sí**       | Ninguno                                         | Revela la rotación y la rotación                          |
| **Buscando**              | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Revela la rotación y la rotación (animación \* de bucle)    |
| **Mostrar**                   | Ninguno                     | No                | **Sí**       | **Mostrando**                                  | Mossos en                                               |
| **StartListening**         | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Coloca la mano al oído                                       |
| **StopListening**          | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Manos a la cabeza                                     |
| **Sugerir**                | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Muestra la bombilla                                    |
| **Sorprendido**              | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Parece que se ha quedo con la                                        |
| **Pensar**                  | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Busca con ala en la cara                             |
| **Pensando**               | Ninguno                     | No                | **No**        | Ninguno                                         | Busca con el ala en la cara \* (animación de bucle)       |
| **Incierto**              | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Se inclina hacia la derecha y se encoge                              |
| **Onda**                   | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Olas                                                  |
| **Escritura**                  | **WriteReturn**          | Sí               | **Sí**       | Ninguno                                         | Quita lápiz y panel, escribe y busca          |
| **WriteContinued**         | **WriteReturn**          | Sí               | **Sí**       | Ninguno                                         | Escribe y busca                                    |
| **WriteReturn**            | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                            |
| **Escritura**                | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Quita el lápiz y el panel, escribe (animación \* de bucle) |



 

\* Si reproduce una animación en bucle, debe usar [**Detener**](stop-method.md) para borrarla antes de que se reprodguen otras animaciones de la cola del carácter.

 

