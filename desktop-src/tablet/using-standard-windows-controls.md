---
description: Use controles Windows estándar siempre que sea posible, ya que son totalmente compatibles con las Microsoft Active Accessibility estándar. Esto incluye los controles proporcionados por Windows (User32.dll) y la biblioteca Windows controles comunes (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Uso de controles Windows estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71beab38b4ee6ea6472a34b4edb190deed97731496eac7101859a9340c65ad0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449278"
---
# <a name="using-standard-windows-controls"></a>Uso de controles Windows estándar

Use controles Windows estándar siempre que sea posible, ya que son totalmente compatibles con las Microsoft Active Accessibility estándar. Esto incluye los controles proporcionados por Windows (User32.dll) y la biblioteca Windows controles comunes (Comctl32.dll).

Cada control Windows estándar es una ventana independiente de una clase específica, por lo que la ayuda de accesibilidad se notifica cuando el foco se mueve a un nuevo control. La ayuda puede determinar la clase de ventana de controles y los mensajes adicionales que puede enviar para consultar o modificar el estado de los controles. La ayuda también puede identificar todos los controles secundarios incluidos en una ventana primaria e identificar el elemento primario de cualquier control.

Algunos controles comunes son extremadamente flexibles y a menudo pueden sustituir por controles personalizados menos accesibles y controles dibujados por el propietario. Por ejemplo, una vista de lista puede reemplazar un cuadro de lista dibujado por el propietario para mostrar una casilla junto a cada elemento. Como otro ejemplo, el control de botón mejorado puede mostrar imágenes y texto. Anteriormente, esto requería el uso de un control personalizado.

 

 



