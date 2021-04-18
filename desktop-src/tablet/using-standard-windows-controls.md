---
description: Use los controles estándar de Windows siempre que sea posible, ya que son totalmente compatibles con las directrices de Microsoft Active Accessibility. Esto incluye los controles proporcionados por Windows (User32.dll) y la biblioteca de controles comunes de Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Usar controles estándar de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360256"
---
# <a name="using-standard-windows-controls"></a>Usar controles estándar de Windows

Use los controles estándar de Windows siempre que sea posible, ya que son totalmente compatibles con las directrices de Microsoft Active Accessibility. Esto incluye los controles proporcionados por Windows (User32.dll) y la biblioteca de controles comunes de Windows (Comctl32.dll).

Cada control estándar de Windows es una ventana independiente de una clase específica, por lo que se notifica a la ayuda de accesibilidad cuando el foco se mueve a un nuevo control. La ayuda puede determinar la clase de ventana controles y los mensajes adicionales que puede enviar para consultar o modificar el estado de los controles. La ayuda también puede identificar todos los controles secundarios incluidos en una ventana primaria e identificar el elemento primario de cualquier control.

Algunos controles comunes son extremadamente flexibles y a menudo pueden sustituirse por controles personalizados y controles dibujados por el propietario menos accesibles. Por ejemplo, una vista de lista puede reemplazar un cuadro de lista dibujado por el propietario para mostrar una casilla junto a cada elemento. Como otro ejemplo, el control de botón mejorado puede mostrar imágenes y texto. Anteriormente, esto requería el uso de un control personalizado.

 

 



