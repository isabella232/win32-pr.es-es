---
title: Componentes
description: Componentes
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL en Windows,components
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161119"
---
# <a name="components"></a>Componentes

La implementación de Microsoft de OpenGL en Windows incluye los siguientes componentes:

-   Conjunto completo de comandos OpenGL actuales

    OpenGL contiene una biblioteca de funciones principales para operaciones de gráficos 3D. Estas funciones básicas se usan para administrar la descripción de las formas de los objetos, la transformación de la matriz, la iluminación, el color, la textura, el recorte, los mapas de bits, la textura y el suavizado de contorno. Los nombres de estas funciones principales tienen un prefijo "gl".

    Muchos de los comandos de OpenGL tienen varias variantes, que difieren en el número y el tipo de sus parámetros. Contando todas las variantes, hay más de 300 comandos OpenGL.

-   Biblioteca de la utilidad OpenGL (GLU)

    Esta biblioteca de funciones auxiliares complementa las funciones principales de OpenGL. Los comandos administran la compatibilidad con texturas, la transformación de coordenadas, la teselación de polígonos, las esferas de representación, los cilindros y los discos, las curvas y las superficies de XSLBS (B-Spline lógica no uniforme) y el control de errores.

-   Biblioteca auxiliar de la guía de programación openGL

    Se trata de una biblioteca de funciones sencilla e independiente de la plataforma para administrar ventanas, controlar eventos de entrada, dibujar objetos 3D clásicos, administrar un proceso en segundo plano y ejecutar un programa. Las rutinas de entrada y administración de ventanas proporcionan un nivel base de funcionalidad con el que puede empezar a programar rápidamente en OpenGL.

    Sin embargo, no los use en una aplicación de producción. Estas son algunas de las razones de esta advertencia:

    -   El bucle de mensajes está en el código de la biblioteca.
    -   No hay ninguna manera de agregar controladores para mensajes WM \* adicionales.
    -   Hay muy poca compatibilidad con las paletas lógicas.

    La biblioteca se describe y usa en la Guía *de programación de OpenGL*.

-   Funciones WGL

    Este conjunto de funciones conecta OpenGL al sistema Windows ventanas. Las funciones administran contextos de representación, listas para mostrar, funciones de extensión y mapas de bits de fuentes. Las funciones de WGL son análogas a las extensiones GLX que conectan OpenGL al sistema de ventanas X. Los nombres de estas funciones tienen un prefijo "wgl".

-   Nuevas Windows para formatos de píxeles y almacenamiento en búfer doble

    Estas funciones admiten formatos de píxeles por ventana y almacenamiento en búfer doble (para cambios de imagen sin problemas) de ventanas. Estas nuevas funciones solo se aplican a las ventanas de gráficos OpenGL.

 

 




