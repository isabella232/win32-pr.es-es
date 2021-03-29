---
title: Animaciones del agente de Microsoft para el carácter Robby
description: Animaciones del agente de Microsoft para el carácter Robby
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347c95fd6a29af72041d3b9e1192167d34602260
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790588"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Animaciones del agente de Microsoft para el carácter Robby

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El [carácter Robby del agente de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) es un trabajo con copyright de Microsoft Corporation.

Robby admite las animaciones que se muestran en la tabla siguiente. Consulte [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) and [Programming the Microsoft Agent control](programming-the-microsoft-agent-control.md) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor [**Get**](get-method.md) o del servidor, tenga en cuenta cómo se descargarán. En lugar de descargar todas las animaciones a la vez, puede que desee recuperar primero las animaciones de estado de **visualización** y de **habla** . Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se desconectan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de animación y de caracteres se cargan correctamente, use el evento [**RequestComplete**](requestcomplete-event.md) . Si se produce un error en una solicitud de carga, puede volver a intentar cargar los datos o mostrar un mensaje adecuado.

Si la animación **devuelta** de una animación se define mediante ramas de salida, no es necesario llamarlo explícitamente. El agente reproduce automáticamente la animación **devuelta** antes de la siguiente animación. Sin embargo, si se muestra una animación de **devolución** , debe llamar a la animación con el método [**Play**](play-method.md) antes de otra animación para proporcionar una transición suave. Si no aparece ninguna animación **devuelta** , la animación finaliza normalmente sin necesidad de una animación transitoria.

El archivo de caracteres incluye efectos sonoros para algunas animaciones, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades del agente de Microsoft. También puede deshabilitar los efectos sonoros en la aplicación.



| Animación                 | Devolver animación         | Admite hablar | Efectos sonoros | Asignado a estado                            | Descripción                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Confirmación**           | None                     | No                | **No**        | None                                         | Encabezado nodos                                                  |
| **Alerta**                 | Sí, usar ramas de salida | Sí               | **No**        | **Escucha**                                | Straight                                                |
| **Anuncie**              | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Imprime papel e informes                               |
| **Blink**                 | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadeos                                                |
| **Confusión**              | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Cabeza de arañazos                                             |
| **Felicitar**          | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Lanza a manos de la mano                             |
| **Rechazar**               | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Levanta la mano y sacudirá el cabezal                                |
| **DoMagic1**              | None                     | Sí               | **No**        | None                                         | Quita el dispositivo                                             |
| **DoMagic2**              | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Aparece un botón y un haz                            |
| **DontRecognize**         | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Incluye mano a las lengüetas                                          |
| **Explicación**               | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Gestos con brazos                                         |
| **GestureDown**           | Sí, usar ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                              |
| **GestureLeft**           | Sí, usar ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                              |
| **GestureRight**          | Sí, usar ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                             |
| **GestureUp**             | Sí, usar ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                                |
| **GetAttention**          | **GetAttentionReturn**   | Sí               | **No**        | None                                         | Ramas de olas                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sí               | **No**        | None                                         | Ramas de nuevo                                           |
| **GetAttentionReturn**    | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                |
| **Acogida**                 | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Mantiene la mano                                              |
| **Audición \_ 1**            | Sí, usar ramas de salida | No                | **No**        | **Oído**                                  | Inclinación derecha (animación en \* bucle)                     |
| **Audición \_ 2**            | Sí, usar ramas de salida | No                | **No**        | **Oído**                                  | Inclina la izquierda ( \* animación en bucle)                      |
| **Audición \_ 3**            | Sí, usar ramas de salida | No                | **No**        | **Oído**                                  | Cabezal izquierdo de llaves ( \* animación en bucle)                      |
| **Audición \_ 4**            | Sí, usar ramas de salida | No                | **No**        | **Oído**                                  | Inclinar hacia abajo ( \* animación en bucle)                      |
| **Ocultar**                  | None                     | No                | **Sí**       | **Conde**                                   | Desaparece a través de la puerta                                    |
| **Idle1 \_ 1**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vistazo a la derecha                                              |
| **Idle1 \_ 2**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | El vistazo y los parpadeos                                      |
| **Idle1 \_ 3**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vista rápida y parpadeo                                    |
| **Idle1 \_ 4**              | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Mirar a la izquierda y a los parpadeos                                    |
| **Idle2 \_ 1**              | None                     | No                | **No**        | **IdlingLevel2**                             | Repliegues                                                 |
| **Idle2 \_ 2**              | None                     | No                | **Sí**       | **IdlingLevel2**                             | Quita el encabezado y realiza el ajuste                          |
| **Idle3 \_ 1**              | None                     | No                | **No**        | **IdlingLevel3**                             | Yawns                                                      |
| **Idle3 \_ 2**              | None                     | No                | **Sí**       | **IdlingLevel3**                             | Cerrar                                                 |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | None                                         | Buscar                                                 |
| **LookDownReturn**        | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | None                                         | Aparece a la izquierda                                                 |
| **LookLeftReturn**        | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | None                                         | Parece correcto                                                |
| **LookRightReturn**       | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                |
| **Buscar**                | **LookUpReturn**         | No                | **No**        | None                                         | Busca                                                   |
| **LookUpReturn**          | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                |
| **Bajar**              | Sí, usar ramas de salida | No                | **Sí**       | **MovingDown**                               | Volar                                                 |
| **MoveLeft**              | Sí, usar ramas de salida | No                | **Sí**       | **MovingLeft**                               | Volar a la izquierda                                                 |
| **Anula**             | Sí, usar ramas de salida | No                | **Sí**       | **MovingRight**                              | Volar a la derecha                                                |
| **MoveUp**                | Sí, usar ramas de salida | No                | **Sí**       | **MovingUp**                                 | Volar                                                   |
| **Satisfechos**               | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Sonrisas y rectas                                  |
| **Proceso**               | No                       | No                | **Sí**       | None                                         | Presiona botones, impresiones, lecturas y, después, muestra una copia impresa       |
| **Processing**            | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Presiona botones, impresiones, lecturas y, después, muestra una copia impresa       |
| **Lectura**                  | **ReadReturn**           | Sí               | **Sí**       | None                                         | Imprime, Lee y busca                                |
| **ReadContinued**         | **ReadReturn**           | Sí               | **Sí**       | None                                         | Lee y busca                                         |
| **ReadReturn**            | None                     | No                | **Sí**       | None                                         | Vuelve a la posición neutra                                |
| **Leía**               | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Imprime, Lee y busca (animación en \* bucle)          |
| **RestPose**              | None                     | Sí               | **No**        | **Habla**                                 | Posición neutra                                           |
| **San**                   | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Sad (expresión)                                             |
| **Búsqueda**                | No                       | No                | **Sí**       | None                                         | Revela el cuadro de herramientas y quita la herramienta                           |
| **Buscándol**             | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Revela el cuadro de herramientas y quita las herramientas ( \* animación en bucle)    |
| **Mostrar**                  | None                     | No                | **Sí**       | **Mostrando**                                  | Aparece a través de la puerta                                    |
| **StartListening**        | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Coloca la mano en el oído                                           |
| **StopListening**         | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Pone a mano los oídos                                       |
| **Sugerir**               | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Muestra bombilla                                         |
| **Sorprendido**             | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Aspecto sorprendido                                            |
| **Opina**                 | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Cabeza de arañazos                                             |
| **Pensando**              | No                       | No                | **Sí**       | None                                         | Encabezado de arañazos ( \* animación en bucle)                       |
| **Seguro**             | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Shrugs                                                     |
| **Ondas**                  | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Ondas                                                      |
| **Escritura**                 | **WriteReturn**          | Sí               | **Sí**       | None                                         | Revela el lápiz y el portapapeles, escribe y busca          |
| **WriteContinued**        | **WriteReturn**          | Sí               | **Sí**       | None                                         | Escribe y busca                                        |
| **WriteReturn**           | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                                |
| **Escribir**               | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Revela el lápiz y el portapapeles, escrituras ( \* animación en bucle) |



 

\* Si reproduce una animación de bucle, debe utilizar [**detener**](stop-method.md) para borrarla antes de que se reproduzcan otras animaciones en la cola del carácter.

 

