---
title: Modelo de ejecución
description: Modelo de ejecución
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modelo de ejecución
- modelo de ejecución OpenGL
- OpenGL, modelo cliente/servidor
- modelo de cliente/servidor OpenGL
- OpenGL, transparente en red
- framebuffers, modelo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994489"
---
# <a name="execution-model"></a>Modelo de ejecución

El modelo para la interpretación de comandos OpenGL es cliente/servidor. Código de la aplicación (el cliente) emite comandos, que se interpretan y procesan con OpenGL (el servidor). El servidor puede funcionar o no en el mismo equipo que el cliente. En este sentido, OpenGL es transparente en la red. Un servidor puede mantener varios contextos de OpenGL, cada uno de los cuales es un estado de OpenGL encapsulado. Un cliente puede conectarse a uno de estos contextos. El protocolo de red necesario se puede implementar aumentando un protocolo ya existente (por ejemplo, el del sistema de ventanas X) o mediante un protocolo independiente. No se proporciona ningún comando OpenGL para obtener datos proporcionados por el usuario.

En última instancia, el sistema de ventanas que asigna recursos fotogramas controla los efectos de los comandos OpenGL en el fotogramas. El sistema de Windows:

-   Determina a qué partes de fotogramas OpenGL puede tener acceso en un momento dado.
-   Se comunica con OpenGL cómo se estructuran esas partes.

Por lo tanto, no hay comandos OpenGL para configurar el fotogramas o inicializar OpenGL. La configuración del búfer de fotogramas se realiza fuera de OpenGL junto con el sistema de ventanas; La inicialización de OpenGL tiene lugar cuando el sistema de ventanas asigna una ventana para la representación de OpenGL.

 

 




