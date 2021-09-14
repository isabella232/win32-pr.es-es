---
title: Estados de los botones
description: En esta sección se describe cómo la selección de un botón cambia su estado y cómo debe responder la aplicación.
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174002"
---
# <a name="button-states"></a>Estados de los botones

En esta sección se describe cómo la selección de un botón cambia su estado y cómo debe responder la aplicación.

La sección consta de los temas siguientes:

-   [Selección de botón](#button-selection)
-   [Elementos de un estado de botón](#elements-of-a-button-state)
    -   [Estado de enfoque](#focus-state)
    -   [Estado de inserción](#push-state)
    -   [Comprobar estado](#check-state)
-   [Cambios en un estado de botón](#changes-to-a-button-state)

## <a name="button-selection"></a>Selección de botón

El usuario puede seleccionar un botón de tres maneras: haciendo clic en él con el mouse, con tabulación hasta él y, a continuación, presionando la tecla ENTRAR, o (si el botón forma parte de un grupo definido por el estilo de grupo de [**WS) \_**](/windows/desktop/winmsg/window-styles) mediante la tabulación al botón seleccionado del grupo y el uso de las teclas de dirección para moverse dentro de ese grupo. Los dos métodos de tabulación forman parte de la interfaz de teclado predefinida proporcionada por el sistema. Para obtener una descripción completa de esta interfaz, vea [Cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes).

La selección de un botón suele provocar los siguientes eventos:

-   El sistema proporciona al botón el foco del teclado.
-   El botón envía un mensaje a su ventana primaria para notificarle la selección.
-   La ventana primaria (o el sistema) envía al botón un mensaje para cambiar su estado.
-   La ventana primaria (o el sistema) vuelve a dibujar el botón para reflejar su nuevo estado.

## <a name="elements-of-a-button-state"></a>Elementos de un estado de botón

El estado de un botón se puede caracterizar por su estado de enfoque, el estado de inserción y el estado de comprobación.

-   [Estado de enfoque](#focus-state)
-   [Estado de inserción](#push-state)
-   [Comprobar estado](#check-state)

### <a name="focus-state"></a>Estado de enfoque

El estado de foco se aplica a una casilla, un botón de radio, un botón de inserción o un botón dibujado por el propietario. Un botón recibe el foco del teclado cuando el usuario lo selecciona y pierde el foco cuando el usuario selecciona otro control. Solo un control puede tener el foco del teclado a la vez.

Cuando un botón tiene el foco del teclado, el sistema normalmente resalta el texto, el icono o el mapa de bits de un botón al rodear con una línea de puntos. Además, un botón de inserción tiene un borde oscuro pesado cuando tiene el foco. El sistema cambia automáticamente el resaltado de un botón automático, pero la aplicación debe cambiar el resaltado de un botón no automático mediante el envío de mensajes.

### <a name="push-state"></a>Estado de inserción

El estado de inserción se aplica a un botón de inserción, una casilla, un botón de radio o una casilla de tres estados, pero no se aplica a otros botones. El estado de inserción de un botón se puede insertar o no insertar. Cuando se inserta un botón de inserción (o cualquier botón con el estilo [**\_ PUSHLIKE de BS),**](button-styles.md) el botón se dibuja como un botón bloqueado. Cuando no se inserta, se dibuja como un botón elevado. Cuando se hace clic en una casilla, un botón de radio o una casilla de tres estados, el fondo del botón aparece atenuado. Cuando no se inserta, el fondo del botón no aparece atenuado.

### <a name="check-state"></a>Comprobar estado

El estado de comprobación se aplica a una casilla, un botón de radio o una casilla de tres estados, pero no se aplica a otros botones. El estado se puede comprobar, borrar o (para las casillas de tres estados) indeterminado. Se marca una casilla cuando contiene una marca de verificación y se desactiva cuando no lo hace. Se comprueba un botón de radio cuando contiene un punto negro; se borra cuando no lo hace. Se marca una casilla de tres estados cuando contiene una marca de verificación, se desactiva cuando no lo hace y es indeterminada cuando contiene un cuadro atenuado. El sistema cambia automáticamente el estado de comprobación de un botón automático, pero la aplicación debe cambiar el estado de comprobación de un botón no automático.

## <a name="changes-to-a-button-state"></a>Cambios en un estado de botón

Cuando el usuario selecciona un botón, por lo general es necesario cambiar uno o varios de los elementos de estado del botón. El sistema cambia automáticamente el estado de foco de todos los tipos de botón, el estado de inserción de los botones de inserción o botones con el estilo [**\_ BS PUSHLIKE**](button-styles.md) y el estado de comprobación de todos los botones automáticos. La aplicación debe realizar todos los demás cambios de estado, teniendo en cuenta el tipo, el estilo y el estado actual del botón. En la lista siguiente se muestran los elementos de estado que se deben cambiar para cada tipo de botón:

-   Una casilla debe cambiar el estado de la comprobación.
-   Un botón de radio debe cambiar el estado de comprobación. También puede ser necesario cambiar el estado de comprobación de otros botones de radio del mismo grupo para garantizar la naturaleza mutuamente excluyente de los botones de radio.
-   Dado que el estado de un botón dibujado por el propietario depende de la aplicación, lo que la aplicación debe cambiar en el botón puede variar. No se debe cambiar ningún elemento de un cuadro de grupo, porque los usuarios no pueden seleccionar cuadros de grupo.

Una aplicación puede determinar el estado de un botón enviándole un mensaje [**\_ BM GETCHECK**](bm-getcheck.md) o [**BM \_ GETSTATE;**](bm-getstate.md) la aplicación puede establecer el estado de un botón enviándole un mensaje [**BM \_ SETCHECK**](bm-setcheck.md) o [**BM \_ SETSTATE.**](bm-setstate.md)

 

 