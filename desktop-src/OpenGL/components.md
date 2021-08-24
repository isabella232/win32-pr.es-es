---
title: Componentes
description: Componentes
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL en Windows,components
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11c8d23130393102f39b716e16c0a6433a40122ad176a525b40e2e1a21b0360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868785"
---
# <a name="components"></a>Componentes

La implementación de OpenGL de Microsoft en Windows incluye los siguientes componentes:

-   Conjunto completo de comandos de OpenGL actuales

    OpenGL contiene una biblioteca de funciones principales para operaciones de gráficos 3D. Estas funciones básicas se usan para administrar la descripción de la forma del objeto, la transformación de la matriz, la iluminación, el coloreo, la textura, el recorte, los mapas de bits, el contorno y el suavizado de contorno. Los nombres de estas funciones principales tienen un prefijo "gl".

    Muchos de los comandos de OpenGL tienen varias variantes, que difieren en el número y el tipo de sus parámetros. Contando todas las variantes, hay más de 300 comandos OpenGL.

-   Biblioteca de la utilidad OpenGL (GLU)

    Esta biblioteca de funciones auxiliares complementa las funciones principales de OpenGL. Los comandos administran la compatibilidad con texturas, la transformación de coordenadas, la teselación de polígonos, las esferas de representación, los cilindros y los discos, las curvas y las superficies DE LA base de datos natural no uniforme (B-Spline no uniforme) y el control de errores.

-   Biblioteca auxiliar de la guía de programación de OpenGL

    Se trata de una biblioteca de funciones sencilla e independiente de la plataforma para administrar ventanas, controlar eventos de entrada, dibujar objetos 3D clásicos, administrar un proceso en segundo plano y ejecutar un programa. Las rutinas de entrada y administración de ventanas proporcionan un nivel base de funcionalidad con el que puede empezar a programar rápidamente en OpenGL.

    Sin embargo, no los use en una aplicación de producción. Estas son algunas de las razones de esta advertencia:

    -   El bucle de mensajes está en el código de la biblioteca.
    -   No hay ninguna manera de agregar controladores para mensajes WM \* adicionales.
    -   Hay muy poca compatibilidad con las paletas lógicas.

    La biblioteca se describe y usa en la Guía *de programación de OpenGL*.

-   Funciones WGL

    Este conjunto de funciones conecta OpenGL al sistema Windows ventanas. Las funciones administran contextos de representación, listas de presentación, funciones de extensión y mapas de bits de fuente. Las funciones WGL son análogas a las extensiones GLX que conectan OpenGL al sistema de ventanas X. Los nombres de estas funciones tienen un prefijo "wgl".

-   Nuevas Windows para formatos de píxeles y almacenamiento en búfer doble

    Estas funciones admiten formatos de píxel por ventana y almacenamiento en búfer doble (para cambios de imagen sin problemas) de las ventanas. Estas nuevas funciones solo se aplican a las ventanas de gráficos OpenGL.

 

 




