---
title: Animaciones de Microsoft Agent para el carácter descarado
description: Animaciones de Microsoft Agent para el carácter descarado
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef6cf0fc3d44f9783fe3d22f9f0d2b291e6acc51bd5bb72890af793ffe55156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609105"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Animaciones de Microsoft Agent para el carácter descarado

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El [carácter Descuido del agente de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) es un trabajo protegido por derechos de Microsoft Corporation.

En la tabla siguiente se admiten animaciones. Consulte Programming the Microsoft Agent Server Interface (Programación de la interfaz del servidor de [Microsoft Agent)](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) y [Programming the Microsoft Agent Control (Programación](programming-the-microsoft-agent-control.md) del control de agente de Microsoft) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método [**Get**](get-method.md) o [**prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor del control, considere cómo las descargará. En lugar de descargar todas las animaciones a  la vez, puede que desee recuperar primero las animaciones de estado **Mostrando** y Hablando. Esto le permitirá mostrar el carácter rápidamente y hacer que se diga mientras se desanan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de caracteres y animaciones se cargan correctamente, use el [**evento RequestComplete.**](requestcomplete-event.md) Si se produce un error en una solicitud de carga, puede volver a cargar los datos o mostrar un mensaje adecuado.

Si la animación **Return** de una animación se define mediante ramas exit, no es necesario llamarla explícitamente. El Agente reproduce automáticamente la **animación Devolución** antes de la animación siguiente. Sin embargo, si aparece **una animación Return,** debe llamar a la animación mediante el método [**Play**](play-method.md) antes de otra animación para proporcionar una transición sin problemas. Si no **aparece ninguna** animación Return, la animación normalmente finaliza sin necesidad de una animación de transición.

El archivo de caracteres incluye efectos de sonido para algunas animaciones, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades de Microsoft Agent. También puede deshabilitar los efectos de sonido en la aplicación.



| Animación                 | Animación de devolución         | Admite habla | Efectos de sonido | Asignado al estado                            | Descripción                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Confirmación**           | Ninguno                     | No                | **No**        | Ninguno                                         | Cabeza de nods                                                  |
| **Alerta**                 | Sí, mediante ramas de salida | Sí               | **No**        | **Escuchar**                                | Endereza                                                |
| **Anunciar**              | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Imprime papel e informes                               |
| **Blink**                 | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadea los ojos                                                |
| **Confusión**              | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Cabeza de scratches                                             |
| **Felicitar**          | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Se elevan las manos y luego se atasman las manos.                             |
| **Rechazar**               | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Eleva la mano y agite la cabeza                                |
| **DoMagic1**              | Ninguno                     | Sí               | **No**        | Ninguno                                         | Quita el dispositivo                                             |
| **DoMagic2**              | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Presiona el botón y aparece el haz.                            |
| **No reconoce**         | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Mano a oído                                          |
| **Explicación**               | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Gestos con los brazos                                         |
| **GestureDown**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                              |
| **GestureLeft**           | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                              |
| **GestureRight**          | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                             |
| **GestureUp**             | Sí, mediante ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                                |
| **GetAttention**          | **GetAttentionReturn**   | Sí               | **No**        | Ninguno                                         | Ondas en las manos                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sí               | **No**        | Ninguno                                         | Ondas de nuevo                                           |
| **GetAttentionReturn**    | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                |
| **Acogida**                 | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Se mantiene al día                                              |
| **Audiencia \_ 1**            | Sí, mediante ramas de salida | No                | **No**        | **Oído**                                  | Inclina la derecha de la cabeza \* (animación de bucle)                     |
| **Audiencia \_ 2**            | Sí, mediante ramas de salida | No                | **No**        | **Oído**                                  | Inclina la cabeza izquierda \* (animación de bucle)                      |
| **Audiencia \_ 3**            | Sí, mediante ramas de salida | No                | **No**        | **Oído**                                  | Esquinas a la izquierda \* (animación de bucle)                      |
| **Audiencia \_ 4**            | Sí, mediante ramas de salida | No                | **No**        | **Oído**                                  | Inclina la cabeza hacia abajo \* (animación de bucle)                      |
| **Ocultar**                  | Ninguno                     | No                | **Sí**       | **Escondiendo**                                   | Desaparece por la puerta                                    |
| **Idle1 \_ 1**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | De un vistazo a la derecha                                              |
| **Idle1 \_ 2**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia arriba y parpadeos                                      |
| **Idle1 \_ 3**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas hacia abajo y parpadeos                                    |
| **Idle1 \_ 4**              | Ninguno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Miradas a la izquierda y parpadeos                                    |
| **Idle2 \_ 1**              | Ninguno                     | No                | **No**        | **IdlingLevel2**                             | Plega los manos                                                 |
| **Idle2 \_ 2**              | Ninguno                     | No                | **Sí**       | **IdlingLevel2**                             | Quita la cabeza y realiza el ajuste.                          |
| **Idle3 \_ 1**              | Ninguno                     | No                | **No**        | **IdlingLevel3**                             | Bostezos                                                      |
| **Idle3 \_ 2**              | Ninguno                     | No                | **Sí**       | **IdlingLevel3**                             | Cierra                                                 |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | Ninguno                                         | Busca hacia abajo.                                                 |
| **LookDownReturn**        | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | Ninguno                                         | Se ve a la izquierda                                                 |
| **LookLeftReturn**        | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | Ninguno                                         | Parece correcto                                                |
| **LookRightReturn**       | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                |
| **Búsqueda**                | **LookUpReturn**         | No                | **No**        | Ninguno                                         | Busca                                                   |
| **LookUpReturn**          | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                |
| **MoveDown**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingDown**                               | Abalo desa,                                                 |
| **MoveLeft**              | Sí, mediante ramas de salida | No                | **Sí**       | **MovingLeft**                               | A la izquierda                                                 |
| **MoveRight**             | Sí, mediante ramas de salida | No                | **Sí**       | **MovingRight**                              | Derecho de las derechas                                                |
| **MoveUp**                | Sí, mediante ramas de salida | No                | **Sí**       | **MovingUp**                                 | A la intesa                                                   |
| **complacido**               | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Sonriente y se endereza                                  |
| **Process**               | No                       | No                | **Sí**       | Ninguno                                         | Presiona botones, imprime, lee y, a continuación, lanza la impresión.       |
| **Procesamiento**            | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Presiona botones, imprime, lee y, a continuación, lanza la impresión.       |
| **Lectura**                  | **ReadReturn**           | Sí               | **Sí**       | Ninguno                                         | Imprime, lee y busca                                |
| **ReadContinued**         | **ReadReturn**           | Sí               | **Sí**       | Ninguno                                         | Lee y busca                                         |
| **ReadReturn**            | Ninguno                     | No                | **Sí**       | Ninguno                                         | Vuelve a la posición neutra                                |
| **Lectura**               | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Imprime, lee y busca (animación \* de bucle)          |
| **RestPose**              | Ninguno                     | Sí               | **No**        | **Hablando**                                 | Posición neutra                                           |
| **Triste**                   | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Expresión desafortunada                                             |
| **Búsqueda**                | No                       | No                | **Sí**       | Ninguno                                         | Revela el cuadro de herramientas y quita la herramienta                           |
| **Buscando**             | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Revela el cuadro de herramientas y quita las herramientas (animación \* de bucle)    |
| **Mostrar**                  | Ninguno                     | No                | **Sí**       | **Mostrando**                                  | Aparece a través de la puerta                                    |
| **StartListening**        | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Coloca la mano al oído                                           |
| **StopListening**         | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Coloca las manos sobre las manos                                       |
| **Sugerir**               | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Muestra bombilla                                         |
| **Sorprendido**             | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Parece que se ha quedo con la                                            |
| **Pensar**                 | Sí, mediante ramas de salida | Sí               | **Sí**       | Ninguno                                         | Cabeza de scratches                                             |
| **Pensando**              | No                       | No                | **Sí**       | Ninguno                                         | Cabeza de scratches \* (animación de bucle)                       |
| **Incierto**             | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Shrugs                                                     |
| **Onda**                  | Sí, mediante ramas de salida | Sí               | **No**        | Ninguno                                         | Olas                                                      |
| **Escritura**                 | **WriteReturn**          | Sí               | **Sí**       | Ninguno                                         | Revela lápiz y portapapeles, escribe y busca          |
| **WriteContinued**        | **WriteReturn**          | Sí               | **Sí**       | Ninguno                                         | Escribe y busca                                        |
| **WriteReturn**           | Ninguno                     | No                | **No**        | Ninguno                                         | Vuelve a la posición neutra                                |
| **Escritura**               | Sí, mediante ramas de salida | No                | **Sí**       | Ninguno                                         | Revela lápiz y portapapeles, escribe (animación \* de bucle) |



 

\* Si reproduce una animación en bucle, debe usar [**Detener**](stop-method.md) para borrarla antes de que se reprodguen otras animaciones de la cola del carácter.

 

