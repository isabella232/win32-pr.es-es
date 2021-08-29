---
title: Ventana de MCIWnd Interfaz de usuario
description: Ventana de MCIWnd Interfaz de usuario
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b58661e46792675b0c2a23dd4ec1d9b98bca1a7bc84d16368595406be3f690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783360"
---
# <a name="mciwnd-window-user-interface"></a>Ventana de MCIWnd Interfaz de usuario

MCIWnd proporciona características adicionales para ajustar el aspecto de la ventana de MCIWnd, personalizar el comportamiento de la aplicación y optimizar el rendimiento de la reproducción. Las siguientes características se incluyen en la ventana MCIWnd:

-   Una barra de herramientas **con los botones Reproducir,** **Detener,** **Grabar** **y Menú**
-   Barra de seguimiento que controla la posición dentro del contenido de reproducción
-   Menú emergente que contiene comandos comunes
-   Un área de reproducción para vídeo y otros dispositivos que muestran imágenes

En la ilustración siguiente se muestra el estado inicial de la reproducción de vídeo controlada por el usuario. El archivo de ejemplo utilizado es CLOCK.AVI.

![clock.avi imagen](images/mciwnd1.gif)

La ventana MCIWnd incluye un área de reproducción para vídeo y otros dispositivos que muestran imágenes durante la reproducción. MCIWnd omite el área de reproducción de los dispositivos de audio de forma de onda, secuenciadores MIDI y otros dispositivos que no escriben en la pantalla. En la ilustración siguiente se muestra el área de reproducción de audio de forma de onda.

![Imagen de ventana mciwnd](images/mciwnd4.gif)

El **botón** Reproducir se encuentra en la esquina inferior izquierda de la ventana MCIWnd. Aparece cuando se detiene el contenido. El usuario puede reproducir el contenido de las maneras siguientes:

-   Para reproducir el contenido desde la posición de reproducción actual, seleccione el **botón Reproducir.**
-   Para reproducir el contenido a pantalla completa desde la posición de reproducción actual, seleccione el botón **Reproducir** mientras mantiene presionada la tecla CTRL.
-   Para reproducir el contenido hacia atrás desde la posición de reproducción actual, seleccione el **botón Reproducir** mientras mantiene presionada la tecla MAYÚS.

El **botón** Menú, situado  junto al botón Reproducir, activa un menú que permite al usuario abrir y cerrar archivos intercalados de audio y vídeo (AVI) y ajustar el tamaño de la imagen, la velocidad de reproducción y el volumen. (El usuario también puede activar el menú haciendo clic con el botón derecho del mouse cada vez que el cursor se encuentra en el área cliente de la ventana). El menú también incluye comandos para cambiar la configuración del dispositivo actual, copiar el contenido de reproducción en el Portapapeles y emitir comandos MCI.

La barra de seguimiento a la derecha del botón **Menú** representa la duración del contenido de reproducción (o grabado). El control deslizante de la barra de seguimiento representa la posición de reproducción actual dentro del contenido. Cuando el control deslizante se coloca en el extremo izquierdo de la barra de seguimiento, la posición de reproducción actual es el principio del contenido. El usuario puede moverse a diferentes ubicaciones del contenido arrastrando el control deslizante a lo largo de la barra de seguimiento. El **botón** Detener se encuentra en la esquina inferior izquierda de la ventana MCIWnd. Aparece cuando se reproduce el contenido. En la ilustración siguiente se muestra la reproducción de vídeo en curso.

![imagen de reproducción de vídeo](images/mciwnd2.gif)

Los controles MCIWnd también pueden incluir un **botón Registro** para los dispositivos que pueden grabar. El **botón** Grabar está marcado con un círculo rojo y solo aparece cuando el dispositivo es capaz de grabar.

> [!Note]  
> La ventana de reproducción debe estar alineada en un límite de cuatro píxeles para obtener el mejor rendimiento de reproducción de vídeo. Normalmente, Windows alinea automáticamente la ventana cuando se crea. Si un usuario mueve o extiende la ventana desde su posición inicial, la velocidad de reproducción de vídeo podría reducirse a la mitad.

 

 

 




