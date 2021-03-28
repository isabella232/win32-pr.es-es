---
description: Los cambios en la paleta del sistema para el dispositivo de pantalla pueden tener efectos drásticos y a veces no deseados en los colores utilizados en Windows en el escritorio.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Mensajes de la paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f19a5458ec89d8d9a0524fd2ec383de740c0179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984886"
---
# <a name="palette-messages"></a>Mensajes de la paleta

Los cambios en la paleta del sistema para el dispositivo de pantalla pueden tener efectos drásticos y a veces no deseados en los colores utilizados en Windows en el escritorio. Para minimizar el impacto de estos cambios, el sistema proporciona un conjunto de mensajes que ayudan a las aplicaciones a administrar sus paletas lógicas, a la vez que garantizan que los colores de la ventana activa sean lo más cercanos posible a los colores previstos.

El sistema envía un mensaje de [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) a una ventana de nivel superior o superpuesta justo antes de activar la ventana. Este mensaje proporciona a una aplicación la oportunidad de seleccionar y observar su paleta lógica para que reciba la mejor asignación posible de colores para su paleta lógica. Cuando la aplicación recibe el mensaje, debe usar las funciones [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette), [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para seleccionar y obtener la paleta lógica. Al hacerlo, se indica al sistema que actualice los colores de la paleta del sistema para que sus colores coincidan con tantos colores en la paleta lógica como sea posible.

Cuando una aplicación provoca cambios en la paleta del sistema como resultado de la realidad de la paleta lógica, el sistema envía un mensaje de [**WM \_ PALETTECHANGED**](wm-palettechanged.md) a todas las ventanas superpuestas y de nivel superior. Este mensaje proporciona a las aplicaciones la oportunidad de actualizar los colores de las áreas de cliente de sus ventanas, reemplazando los colores que han cambiado con los colores que coinciden más estrechamente con los colores previstos. Una aplicación que recibe el mensaje de **\_ PALETTECHANGED de WM** debe usar [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para restablecer las paletas lógicas asociadas a todas las ventanas inactivas y, a continuación, actualizar los colores del área cliente para cada ventana inactiva mediante la función [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) . Esta técnica no garantiza el mayor número de coincidencias exactas de color; sin embargo, garantiza que los colores de la paleta lógica estén asignados a colores razonables en la paleta del sistema.

> [!Note]  
> Para evitar la creación de un bucle infinito, una aplicación nunca debe obtener la paleta de la ventana cuyo identificador coincide con el identificador pasado en el parámetro *wParam* del mensaje de [**\_ PALETTECHANGED de WM**](wm-palettechanged.md) .

 

Normalmente, la función [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) actualiza un área cliente de una ventana inactiva más rápido que volver a dibujar el área. Sin embargo, dado que **UpdateColors** realiza la traducción de color en función del color de cada píxel antes de que cambie la paleta del sistema, cada llamada a esta función provoca la pérdida de alguna precisión del color. Esto significa que **UpdateColors** no se puede usar para actualizar los colores cuando la ventana se activa. En tales casos, la aplicación debe volver a dibujar el área cliente.

El sistema puede enviar el mensaje de [**\_ QUERYNEWPALETTE de WM**](wm-querynewpalette.md) cuando se realizan cambios en la paleta lógica. Además, el sistema puede enviar el mensaje de [**\_ PALETTEISCHANGING de WM**](wm-paletteischanging.md) a todas las ventanas superpuestas y de nivel superior cuando la paleta del sistema está a punto de cambiar.

 

 



