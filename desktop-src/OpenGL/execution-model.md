---
title: Modelo de ejecución
description: Modelo de ejecución
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modelo de ejecución
- modelo de ejecución OpenGL
- OpenGL, modelo de cliente/servidor
- modelo cliente/servidor OpenGL
- OpenGL, transparente en la red
- framebuffers,modelo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7cb7c3c06baa0a56f4c59b14744b73962fced369d56f00cbf887b9ae6d09e2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082465"
---
# <a name="execution-model"></a>Modelo de ejecución

El modelo para la interpretación de comandos OpenGL es cliente/servidor. El código de aplicación (el cliente) emite comandos, que OpenGL (el servidor) interpreta y procesa. El servidor puede o no funcionar en el mismo equipo que el cliente. En este sentido, OpenGL es transparente para la red. Un servidor puede mantener varios contextos de OpenGL, cada uno de los cuales es un estado OpenGL encapsulado. Un cliente puede conectarse a cualquiera de estos contextos. El protocolo de red necesario se puede implementar mediante el aumento de un protocolo ya existente (como el del sistema de ventanas X) o mediante un protocolo independiente. No se proporcionan comandos OpenGL para obtener la entrada del usuario.

El sistema de ventanas que asigna recursos de framebuffer controla en última instancia los efectos de los comandos OpenGL en el búfer de fotogramas. El sistema de ventanas:

-   Determina a qué partes del búfer de fotogramas puede tener acceso OpenGL en un momento dado.
-   Comunica a OpenGL cómo se estructuran esas partes.

Por lo tanto, no hay ningún comando OpenGL para configurar el búfer de fotogramas o inicializar OpenGL. La configuración del búfer de fotogramas se realiza fuera de OpenGL junto con el sistema de ventanas; La inicialización de OpenGL tiene lugar cuando el sistema de ventanas asigna una ventana para la representación de OpenGL.

 

 




