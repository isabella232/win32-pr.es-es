---
title: ¿Qué es una ventana?
description: ¿Qué es una ventana?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8494738e3985f78930549f313cb2868b79b34f3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159920"
---
# <a name="what-is-a-window"></a>¿Qué es una ventana?

## <a name="what-is-a-window"></a>¿Qué es una ventana?

Obviamente, las ventanas son fundamentales para Windows. Son tan importantes que han llamado al sistema operativo después de ellos. ¿Pero qué es una ventana? Cuando piense en una ventana, probablemente piense en algo parecido a esto:

![captura de pantalla de una ventana de aplicación](images/window01.png)

Este tipo de ventana se denomina ventana *de aplicación o* ventana *principal.* Normalmente tiene un marco con una barra de título, **botones Minimizar** y **Maximizar** y otros elementos de la interfaz de usuario estándar. El marco se denomina área *no* cliente de la ventana, así que se llama porque el sistema operativo administra esa parte de la ventana. El área dentro del marco es el *área de cliente*. Esta es la parte de la ventana que administra el programa.

Este es otro tipo de ventana:

![captura de pantalla de una ventana de control](images/window02.png)

Si no está nunca Windows programación, puede que le conste de que los controles de interfaz de usuario, como los botones y los cuadros de edición, son ventanas propiamente dichas. La principal diferencia entre un control de interfaz de usuario y una ventana de aplicación es que un control no existe por sí mismo. En su lugar, el control se coloca en relación con la ventana de la aplicación. Al arrastrar la ventana de la aplicación, el control se mueve con ella, como se esperaría. Además, el control y la ventana de la aplicación pueden comunicarse entre sí. (Por ejemplo, la ventana de la aplicación recibe notificaciones de clic de un botón).

Por lo tanto, cuando piense *en la ventana*, no piense simplemente en la ventana de la *aplicación*. En su lugar, piense en una ventana como una construcción de programación que:

-   Ocupa una parte determinada de la pantalla.
-   Puede o no estar visible en un momento dado.
-   Sabe cómo dibujarse a sí mismo.
-   Responde a eventos del usuario o del sistema operativo.

## <a name="parent-windows-and-owner-windows"></a>Propiedad Windows principal y propietario Windows

En el caso de un control de interfaz de usuario, se dice que la ventana de control es *el elemento secundario* de la ventana de aplicación. La ventana de aplicación es *el elemento primario* de la ventana de control. La ventana primaria proporciona el sistema de coordenadas utilizado para colocar una ventana secundaria. Tener una ventana primaria afecta a aspectos de la apariencia de una ventana; Por ejemplo, se recorta una ventana secundaria para que ninguna parte de la ventana secundaria pueda aparecer fuera de los bordes de su ventana primaria.

Otra relación es la relación entre una ventana de aplicación y una ventana de diálogo modal. Cuando una aplicación muestra un cuadro de  diálogo modal, la ventana de la aplicación es la ventana del propietario y el diálogo es una *ventana de* propiedad. Una ventana de propiedad siempre aparece delante de su ventana de propietario. Se oculta cuando el propietario se minimiza y se destruye al mismo tiempo que el propietario.

En la imagen siguiente se muestra una aplicación que muestra un cuadro de diálogo con dos botones:

![captura de pantalla de una aplicación con un cuadro de diálogo](images/window03.png)

La ventana de aplicación es propietaria de la ventana de diálogo y la ventana de diálogo es el elemento primario de ambas ventanas de botón. En el diagrama siguiente se muestran estas relaciones:

![ilustración en la que se muestran las relaciones entre los elementos primarios y secundarios y los propietarios y los propietarios.](images/window04.png)

## <a name="window-handles"></a>Identificadores de ventana

Windows objetos (tienen código y datos), pero no son clases de C++. En su lugar, un programa hace referencia a una ventana mediante un valor denominado *identificador*. Un identificador es un tipo opaco. Básicamente, es solo un número que el sistema operativo usa para identificar un objeto. Puede imaginar que Windows una tabla grande de todas las ventanas que se han creado. Usa esta tabla para buscar ventanas por sus identificadores. (No es importante saber exactamente cómo funciona internamente). El tipo de datos de los identificadores de ventana **es HWND,** que normalmente se pronuncia como "aitch-wind". Las funciones que crean ventanas devuelven identificadores de ventana: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) y [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

Para realizar una operación en una ventana, normalmente llamará a alguna función que toma un **valor HWND** como parámetro. Por ejemplo, para cambiar la posición de una ventana en la pantalla, llame a la [**función MoveWindow:**](/windows/desktop/api/winuser/nf-winuser-movewindow)


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



El primer parámetro es el identificador de la ventana que desea mover. Los demás parámetros especifican la nueva ubicación de la ventana y si se debe volver a dibujar la ventana.

Tenga en cuenta que los identificadores no son punteros. Si *hwnd* es una variable que contiene un identificador, intentar desreferenciar el identificador escribiendo `*hwnd` es un error.

## <a name="screen-and-window-coordinates"></a>Coordenadas de pantalla y ventana

Las coordenadas se miden en píxeles independientes del dispositivo. Tendremos más que decir sobre  la parte independiente del dispositivo de *los* píxeles independientes del dispositivo cuando se deba a los gráficos.

En función de la tarea, puede medir las coordenadas con respecto a la pantalla, con respecto a una ventana (incluido el marco) o con respecto al área cliente de una ventana. Por ejemplo, colocaría una ventana en la pantalla mediante coordenadas de pantalla, pero dibujaría dentro de una ventana mediante coordenadas de cliente. En cada caso, el origen (0, 0) siempre es la esquina superior izquierda de la región.

![ilustración en la que se muestran las coordenadas de pantalla, ventana y cliente](images/coordinates01.png)

## <a name="next"></a>Siguientes

[WinMain: el punto de entrada de la aplicación](winmain--the-application-entry-point.md)

 

 
