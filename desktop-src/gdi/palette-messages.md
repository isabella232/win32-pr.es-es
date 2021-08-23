---
description: Los cambios en la paleta del sistema para el dispositivo de pantalla pueden tener efectos drásticos y, a veces, no deseados en los colores usados en las ventanas del escritorio.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Mensajes de paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a82c5ae2727e9f687f5f7fb628279b7832e896991f703225beec075a6630133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558445"
---
# <a name="palette-messages"></a>Mensajes de paleta

Los cambios en la paleta del sistema para el dispositivo de pantalla pueden tener efectos drásticos y, a veces, no deseados en los colores usados en las ventanas del escritorio. Para minimizar el impacto de estos cambios, el sistema proporciona un conjunto de mensajes que ayudan a las aplicaciones a administrar sus paletas lógicas y, al mismo tiempo, garantiza que los colores de la ventana activa estén lo más cerca posible de los colores previstos.

El sistema envía un [**mensaje \_ WM QUERYNEWPALETTE**](wm-querynewpalette.md) a una ventana de nivel superior o superpuesta justo antes de activar la ventana. Este mensaje ofrece a una aplicación la oportunidad de seleccionar y realizar su paleta lógica para que reciba la mejor asignación posible de colores para su paleta lógica. Cuando la aplicación recibe el mensaje, debe usar las funciones [**SelectPalette,**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para seleccionar y realizar la paleta lógica. Si lo hace, el sistema actualizará los colores de la paleta del sistema para que sus colores coincidan con tantos colores de la paleta lógica como sea posible.

Cuando una aplicación provoca cambios en la paleta del sistema como resultado de la realización de su paleta lógica, el sistema envía un mensaje [**\_ WM PALETTECHANGED**](wm-palettechanged.md) a todas las ventanas de nivel superior y superpuestas. Este mensaje ofrece a las aplicaciones la oportunidad de actualizar los colores de las áreas cliente de sus ventanas, reemplazando los colores que han cambiado por colores que coincidan más estrechamente con los colores previstos. Una aplicación que recibe el mensaje **\_ WM PALETTECHANGED** debe usar [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para restablecer las paletas lógicas asociadas a todas las ventanas inactivas y, a continuación, actualizar los colores del área cliente para cada ventana inactiva mediante la [**función UpdateColors.**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) Esta técnica no garantiza el mayor número de coincidencias de color exactas; sin embargo, garantiza que los colores de la paleta lógica se asignan a colores razonables en la paleta del sistema.

> [!Note]  
> Para evitar la creación de un bucle infinito, una aplicación nunca debe darse cuenta de la paleta de la ventana cuyo identificador coincide con el identificador pasado en el *parámetro wParam* del [**mensaje \_ PALETTECHANGED de WM.**](wm-palettechanged.md)

 

La [**función UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) normalmente actualiza un área cliente de una ventana inactiva más rápido que volver a dibujar el área. Sin embargo, dado que **UpdateColors** realiza la traducción de colores en función del color de cada píxel antes de que cambie la paleta del sistema, cada llamada a esta función produce la pérdida de cierta precisión de color. Esto significa **que UpdateColors** no se puede usar para actualizar los colores cuando la ventana se activa. En tales casos, la aplicación debe volver a dibujar el área de cliente.

El sistema puede enviar el [**mensaje WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) cuando se realizan cambios en la paleta lógica. Además, el sistema puede enviar el mensaje [**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md) a todas las ventanas de nivel superior y superpuestas cuando la paleta del sistema está a punto de cambiar.

 

 



