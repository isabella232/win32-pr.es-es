---
title: Estados del botón
description: En esta sección se describe cómo la selección de un botón cambia su estado y cómo debe responder la aplicación.
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488386"
---
# <a name="button-states"></a>Estados del botón

En esta sección se describe cómo la selección de un botón cambia su estado y cómo debe responder la aplicación.

La sección consta de los siguientes temas:

-   [Selección de botón](#button-selection)
-   [Elementos de un estado de botón](#elements-of-a-button-state)
    -   [Estado de foco](#focus-state)
    -   [Estado de la extracción](#push-state)
    -   [Comprobar estado](#check-state)
-   [Cambios en el estado de un botón](#changes-to-a-button-state)

## <a name="button-selection"></a>Selección de botón

El usuario puede seleccionar un botón de tres maneras: haciendo clic en él con el mouse; para ello, vaya a él y presione la tecla entrar, o (si el botón forma parte de un grupo definido por el estilo de [**\_ grupo de WS**](/windows/desktop/winmsg/window-styles) ), desplácese hasta el botón seleccionado del grupo y utilice las teclas de dirección para desplazarse dentro de ese grupo. Los dos métodos de tabulación forman parte de la interfaz de teclado predefinida que proporciona el sistema. Para obtener una descripción completa de esta interfaz, vea [cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes).

Al seleccionar un botón, normalmente se producen los siguientes eventos:

-   El sistema asigna al botón el foco de teclado.
-   El botón envía a su ventana primaria un mensaje para notificárselo a la selección.
-   La ventana primaria (o el sistema) envía un mensaje al botón para cambiar su estado.
-   La ventana primaria (o el sistema) vuelve a dibujar el botón para reflejar su nuevo estado.

## <a name="elements-of-a-button-state"></a>Elementos de un estado de botón

El estado de un botón se puede caracterizar por el estado del foco, el estado de inserción y el estado de activación.

-   [Estado de foco](#focus-state)
-   [Estado de la extracción](#push-state)
-   [Comprobar estado](#check-state)

### <a name="focus-state"></a>Estado de foco

El estado de foco se aplica a una casilla, botón de radio, botón de inserción o botón dibujado por el propietario. Un botón recibe el foco del teclado cuando el usuario lo selecciona y pierde el foco cuando el usuario selecciona otro control. Solo un control puede tener el foco de teclado a la vez.

Cuando un botón tiene el foco de teclado, el sistema normalmente resalta el texto, el icono o el mapa de bits de un botón arrastrándolo con una línea de puntos. Además, un botón de reenvío tiene un borde oscuro intenso cuando tiene el foco. El sistema cambia automáticamente el resaltado de un botón automático, pero la aplicación debe cambiar el resaltado de un botón no automático mediante el envío de mensajes.

### <a name="push-state"></a>Estado de la extracción

El estado de inserción se aplica a un botón de inserción, casilla, botón de radio o casilla de tres Estados, pero no se aplica a otros botones. El estado de inserción de un botón se puede insertar o no insertar. Cuando se inserta un botón de inserción (o cualquier botón con el estilo [**BS \_ PUSHLIKE**](button-styles.md) ), el botón se dibuja como un botón hundido. Cuando no se inserta, se dibuja como un botón elevado. Cuando se hace clic en una casilla, un botón de radio o una casilla de tres Estados, el fondo del botón está atenuado. Cuando no se inserta, el fondo del botón no está atenuado.

### <a name="check-state"></a>Comprobar estado

El estado de activación se aplica a una casilla, un botón de radio o una casilla de tres Estados, pero no se aplica a otros botones. El estado se puede activar, desactivar o (para las casillas de tres Estados) indeterminado. Una casilla está activada cuando contiene una marca de verificación y se desactiva cuando no lo está. Se comprueba un botón de radio cuando contiene un punto negro; se borra cuando no lo está. Una casilla de tres Estados está activada cuando contiene una marca de verificación, está desactivada cuando no es y es indeterminada cuando contiene un cuadro atenuado. El sistema cambia automáticamente el estado de activación de un botón automático, pero la aplicación debe cambiar el estado de activación de un botón no automático.

## <a name="changes-to-a-button-state"></a>Cambios en el estado de un botón

Cuando el usuario selecciona un botón, generalmente es necesario cambiar uno o varios de los elementos de estado del botón. El sistema cambia automáticamente el estado de foco para todos los tipos de botón, el estado de inserción para botones de inserción o botones con el estilo [**BS \_ PUSHLIKE**](button-styles.md) y el estado de activación de todos los botones automáticos. La aplicación debe realizar todos los demás cambios de estado, teniendo en cuenta el tipo, el estilo y el estado actual del botón. En la siguiente lista se muestran los elementos de estado que se deben cambiar para cada tipo de botón:

-   Una casilla debe cambiar el estado de activación.
-   Un botón de radio debe cambiar el estado de activación. También puede ser necesario cambiar el estado de activación de otros botones de radio en el mismo grupo para garantizar la naturaleza mutuamente excluyente de los botones de radio.
-   Dado que el estado de un botón dibujado por el propietario es dependiente de la aplicación, lo que debe cambiar la aplicación en el botón puede variar. No se debe cambiar ningún elemento de un cuadro de grupo, ya que los usuarios no pueden seleccionar cuadros de grupo.

Una aplicación puede determinar el estado de un botón mediante el envío de un mensaje [**BM \_ GETCHECK**](bm-getcheck.md) o [**BM \_ GETSTATE**](bm-getstate.md) ; la aplicación puede establecer el estado de un botón mediante el envío de un mensaje [**BM \_ SETCHECK**](bm-setcheck.md) o [**BM \_ SETSTATE**](bm-setstate.md) .

 

 