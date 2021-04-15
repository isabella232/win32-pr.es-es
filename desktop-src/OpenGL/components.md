---
title: Componentes
description: Componentes
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL en Windows, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676215"
---
# <a name="components"></a>Componentes

La implementación de OpenGL en Windows de Microsoft incluye los siguientes componentes:

-   Conjunto completo de comandos OpenGL actuales

    OpenGL contiene una biblioteca de funciones básicas para las operaciones de gráficos 3D. Estas funciones básicas se usan para administrar la descripción de la forma de objeto, la transformación de matriz, la iluminación, el color, la textura, el recorte, los mapas de bits, la niebla y el suavizado de contorno. Los nombres de estas funciones principales tienen un prefijo "GL".

    Muchos de los comandos OpenGL tienen varias variantes, que difieren en el número y tipo de sus parámetros. Contando todas las variantes, hay más de 300 comandos OpenGL.

-   La biblioteca de la utilidad OpenGL (GLU)

    Esta biblioteca de funciones auxiliares complementa las funciones básicas de OpenGL. Los comandos administran la compatibilidad con texturas, la transformación de coordenadas, la teselación de polígonos, las esferas de representación, los cilindros y los discos, las curvas y superficies de NURBS (no uniforme B-spline racional) y el control de errores.

-   Biblioteca auxiliar de la guía de programación de OpenGL

    Se trata de una biblioteca sencilla, independiente de la plataforma, de funciones para administrar ventanas, controlar los eventos de entrada, dibujar objetos 3D clásicos, administrar un proceso en segundo plano y ejecutar un programa. Las rutinas de entrada y administración de ventanas proporcionan un nivel básico de funcionalidad con el que puede comenzar a programar rápidamente en OpenGL.

    No las use, sin embargo, en una aplicación de producción. Estas son algunas de las razones de esta ADVERTENCIA:

    -   El bucle de mensajes está en el código de la biblioteca.
    -   No hay ninguna manera de agregar controladores para mensajes de WM adicionales \* .
    -   Hay muy poca compatibilidad con las paletas lógicas.

    La biblioteca se describe y se usa en la *Guía de programación de OpenGL*.

-   Las funciones WGL

    Este conjunto de funciones conecta OpenGL al sistema de ventanas de Windows. Las funciones administran los contextos de representación, las listas de visualización, las funciones de extensión y los mapas de bits de fuente. Las funciones WGL son análogas a las extensiones GLX que conectan OpenGL con el sistema de ventana X. Los nombres de estas funciones tienen un prefijo "WGL".

-   Nuevas funciones de Windows para formatos de píxeles y almacenamiento en búfer doble

    Estas funciones admiten formatos de píxel por ventana y doble búfer (para cambios de imagen suaves) de Windows. Estas nuevas funciones solo se aplican a las ventanas de gráficos OpenGL.

 

 




