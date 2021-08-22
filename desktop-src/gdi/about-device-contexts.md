---
description: La independencia de dispositivos es una de las principales características de Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Acerca de los contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9439e3091b3138917e24ab4a49ff89c21a1e1b53480d4a138bd2bbad3288fcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105880"
---
# <a name="about-device-contexts"></a>Acerca de los contextos de dispositivo

La independencia de dispositivos es una de las principales características de Microsoft Windows. Las aplicaciones pueden dibujar e imprimir resultados en una variedad de dispositivos. El software que admite esta independencia del dispositivo se encuentra en dos bibliotecas de vínculos dinámicos. La primera, Gdi.dll, se conoce como la interfaz de dispositivo gráfico (GDI); el segundo se conoce como controlador de dispositivo. El nombre del segundo depende del dispositivo donde la aplicación dibuja la salida. Por ejemplo, si la aplicación dibuja la salida en el área cliente de su ventana en una pantalla VGA, esta biblioteca se Vga.dll; Si la aplicación imprime la salida en una impresora Fx-80 de Fx Fx, esta biblioteca se Epson9.dll.

Una aplicación debe informar a GDI de que cargue un controlador de dispositivo determinado y, una vez cargado el controlador, preparar el dispositivo para las operaciones de dibujo (por ejemplo, seleccionar un color y ancho de línea, un patrón y un color de pincel, un tipo de letra de fuente, una región de recorte, y así sucesivamente). Estas tareas se logran mediante la creación y el mantenimiento de un contexto de dispositivo (DC). Un controlador de dominio es una estructura que define un conjunto de objetos gráficos y sus atributos asociados, así como los modos gráficos que afectan a la salida. Los objetos gráficos incluyen un lápiz para dibujar líneas, un pincel para pintar y rellenar, un mapa de bits para copiar o desplazar partes de la pantalla, una paleta para definir el conjunto de colores disponibles, una región para el recorte y otras operaciones y una ruta de acceso para las operaciones de dibujo y dibujo. A diferencia de la mayoría de las estructuras, una aplicación nunca tiene acceso directo al controlador de dominio; en su lugar, opera en la estructura indirectamente mediante una llamada a varias funciones.

Esta información general proporciona información sobre los temas siguientes:

-   [Objetos gráficos](graphic-objects.md)
-   [Modos gráficos](graphic-modes.md)
-   [Tipos de contexto de dispositivo](device-context-types.md)
-   [Operaciones de contexto de dispositivo](device-context-operations.md)
-   [ICM de contexto de dispositivo habilitadas para dispositivos](icm-enabled-device-context-functions.md)

Un concepto importante es el diseño de un controlador de dominio o una ventana, que describe el orden en el que se revelan los objetos Y el texto GDI (de izquierda a derecha o de derecha a izquierda). Para obtener más información, vea "Diseño y creación de reflejo de ventanas" en [**Características de ventana**](../winmsg/window-features.md) y las funciones [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) [**y SetLayout.**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)

 

 
