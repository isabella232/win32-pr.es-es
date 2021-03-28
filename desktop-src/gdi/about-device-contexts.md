---
description: La independencia de los dispositivos es una de las principales características de Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Acerca de los contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b686ec8b48492658f19531cb42161c043f178d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155205"
---
# <a name="about-device-contexts"></a>Acerca de los contextos de dispositivo

La independencia de los dispositivos es una de las principales características de Microsoft Windows. Las aplicaciones pueden dibujar e imprimir la salida en una variedad de dispositivos. El software que admite esta independencia del dispositivo se encuentra en dos bibliotecas de vínculos dinámicos. La primera, Gdi.dll, se conoce como la interfaz de dispositivo gráfico (GDI). la segunda se conoce como controlador de dispositivo. El nombre del segundo depende del dispositivo en el que la aplicación dibuja la salida. Por ejemplo, si la aplicación dibuja la salida en el área cliente de su ventana en una pantalla VGA, se Vga.dll esta biblioteca; Si la aplicación imprime la salida en una impresora Epson FX-80, esta biblioteca se Epson9.dll.

Una aplicación debe informar a GDI para cargar un controlador de dispositivo determinado y, una vez cargado el controlador, preparar el dispositivo para las operaciones de dibujo (por ejemplo, seleccionar un color y un ancho de línea, un patrón y color de pincel, un tipo de letra de fuente, una región de recorte, etc.). Estas tareas se realizan mediante la creación y el mantenimiento de un contexto de dispositivo (DC). Un controlador de dominio es una estructura que define un conjunto de objetos gráficos y sus atributos asociados, así como los modos gráficos que afectan a la salida. Los objetos gráficos incluyen un lápiz para el dibujo de líneas, un pincel para dibujar y rellenar un mapa de bits para copiar o desplazar partes de la pantalla, una paleta para definir el conjunto de colores disponibles, una región para el recorte y otras operaciones, y una ruta de acceso para dibujar y dibujar operaciones. A diferencia de la mayoría de las estructuras, una aplicación nunca tiene acceso directo al controlador de dominio; en su lugar, funciona en la estructura indirectamente mediante una llamada a varias funciones.

En esta información general se proporciona información sobre los temas siguientes:

-   [Objetos gráficos](graphic-objects.md)
-   [Modos gráficos](graphic-modes.md)
-   [Tipos de contexto de dispositivo](device-context-types.md)
-   [Operaciones de contexto de dispositivo](device-context-operations.md)
-   [Funciones de contexto de dispositivos habilitados para ICM](icm-enabled-device-context-functions.md)

Un concepto importante es el diseño de un controlador de dominio o una ventana, que describe el orden en que se revelan los objetos y el texto GDI (de izquierda a derecha o de derecha a izquierda). Para obtener más información, vea "diseño y creación de reflejo de ventanas" en [**características de Windows**](../winmsg/window-features.md) y las funciones [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) y [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) .

 

 
