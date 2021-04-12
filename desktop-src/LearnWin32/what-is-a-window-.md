---
title: Qué es una ventana
description: .
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fcbba817e3e4c9059340d0a67c7170f4583270c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420603"
---
# <a name="what-is-a-window"></a>¿Qué es una ventana?

## <a name="what-is-a-window"></a>¿Qué es una ventana?

Obviamente, las ventanas son esenciales para Windows. Es tan importante que hayan llamado al sistema operativo después de ellos. Pero, ¿qué es una ventana? Cuando cree una ventana, probablemente piense algo parecido a esto:

![captura de pantalla de una ventana de la aplicación](images/window01.png)

Este tipo de ventana se denomina ventana de la *aplicación* o *ventana principal*. Normalmente tiene un marco con una barra de título, botones **minimizar** y **maximizar** y otros elementos de la interfaz de usuario estándar. El marco se denomina *área no cliente* de la ventana, por lo que se llama a porque el sistema operativo administra esa parte de la ventana. El área dentro del marco es el *área cliente*. Esta es la parte de la ventana que administra el programa.

Este es otro tipo de ventana:

![captura de pantalla de una ventana de control](images/window02.png)

Si no está familiarizado con la programación de Windows, puede sorprenderle de que los controles de interfaz de usuario, como botones y cuadros de edición, son ventanas. La diferencia principal entre un control de interfaz de usuario y una ventana de aplicación es que un control no existe por sí mismo. En su lugar, el control se coloca en relación con la ventana de la aplicación. Al arrastrar la ventana de la aplicación, el control se mueve con ella, como cabría esperar. Además, el control y la ventana de la aplicación pueden comunicarse entre sí. (Por ejemplo, la ventana de la aplicación recibe las notificaciones de clic de un botón).

Por lo tanto, cuando cree una *ventana*, no cree simplemente la ventana de la *aplicación*. En su lugar, piense en una ventana como una construcción de programación que:

-   Ocupa una parte determinada de la pantalla.
-   Puede o no estar visible en un momento dado.
-   Sabe cómo dibujarse a sí mismo.
-   Responde a eventos del usuario o del sistema operativo.

## <a name="parent-windows-and-owner-windows"></a>Ventanas principales y ventanas propietarias

En el caso de un control de interfaz de usuario, se dice que la ventana del control es el *elemento secundario* de la ventana de la aplicación. La ventana de la aplicación es el *elemento primario* de la ventana de control. La ventana primaria proporciona el sistema de coordenadas que se usa para colocar una ventana secundaria. Tener una ventana primaria afecta a aspectos de la apariencia de una ventana; por ejemplo, una ventana secundaria se recorta para que ninguna parte de la ventana secundaria pueda aparecer fuera de los bordes de la ventana primaria.

Otra relación es la relación entre una ventana de la aplicación y una ventana de diálogo modal. Cuando una aplicación muestra un cuadro de diálogo modal, la ventana de la aplicación es la ventana *propietaria* y el cuadro de diálogo es una ventana *propiedad* . Una ventana de propiedad siempre aparece delante de la ventana propietaria. Está oculto cuando el propietario está minimizado y se destruye al mismo tiempo que el propietario.

En la imagen siguiente se muestra una aplicación que muestra un cuadro de diálogo con dos botones:

![captura de pantalla de una aplicación con un cuadro de diálogo](images/window03.png)

La ventana de la aplicación es propietaria de la ventana de cuadro de diálogo y la ventana de cuadro de diálogo es el elemento primario de las dos ventanas de botones. En el diagrama siguiente se muestran estas relaciones:

![Ilustración en la que se muestran las relaciones de elementos primarios y secundarios y propietarios](images/window04.png)

## <a name="window-handles"></a>Identificadores de ventana

Las ventanas son objetos, que tienen código y datos, pero no son clases de C++. En su lugar, un programa hace referencia a una ventana mediante un valor denominado *identificador*. Un identificador es un tipo opaco. Esencialmente, es simplemente un número que el sistema operativo usa para identificar un objeto. Puede crear imágenes de ventanas como una gran tabla de todas las ventanas que se han creado. Usa esta tabla para buscar ventanas por sus identificadores. (Si eso es exactamente como funciona internamente, no es importante). El tipo de datos de los identificadores de ventana es **hWnd**, que normalmente se pronuncia "Aitch". Los identificadores de ventana son devueltos por las funciones que crean Windows: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) y [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).

Para realizar una operación en una ventana, normalmente se llama a una función que toma un valor **hWnd** como parámetro. Por ejemplo, para cambiar la posición de una ventana en la pantalla, llame a la función [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) :


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



El primer parámetro es el identificador de la ventana que desea desplace. Los demás parámetros especifican la nueva ubicación de la ventana y si la ventana debe volver a dibujarse.

Tenga en cuenta que los identificadores no son punteros. Si *hWnd* es una variable que contiene un identificador, el intento de desreferenciar el identificador escribiendo `*hwnd` es un error.

## <a name="screen-and-window-coordinates"></a>Coordenadas de pantalla y ventana

Las coordenadas se miden en píxeles independientes del dispositivo. Tendremos más que decir sobre la parte *independiente del dispositivo* de los *píxeles independientes del dispositivo* cuando se analizan los gráficos.

En función de la tarea, puede medir las coordenadas relativas a la pantalla, con respecto a una ventana (incluido el marco) o con respecto al área de cliente de una ventana. Por ejemplo, puede colocar una ventana en la pantalla mediante las coordenadas de pantalla, pero dibujaría dentro de una ventana con coordenadas de cliente. En cada caso, el origen (0,0) siempre es la esquina superior izquierda de la región.

![Ilustración que muestra las coordenadas de pantalla, ventana y cliente](images/coordinates01.png)

## <a name="next"></a>Siguientes

[WinMain: el punto de entrada de la aplicación](winmain--the-application-entry-point.md)

 

 