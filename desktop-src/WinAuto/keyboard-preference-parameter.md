---
title: Parámetro de preferencias de teclado
description: El parámetro de preferencias de teclado indica que el usuario se basa en el teclado en lugar del mouse, por lo que las aplicaciones deben mostrar las interfaces de teclado que, de otro modo, podrían ocultarse.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420960"
---
# <a name="keyboard-preference-parameter"></a>Parámetro de preferencias de teclado

El parámetro de preferencias de teclado indica que el usuario se basa en el teclado en lugar del mouse, por lo que las aplicaciones deben mostrar las interfaces de teclado que, de otro modo, podrían ocultarse.

El usuario controla el valor del parámetro de preferencias de teclado mediante el centro de accesibilidad del panel de control u otra aplicación para personalizar el entorno. Las aplicaciones usan las marcas **SPI \_ GETKEYBOARDPREF** y **SPI \_ SETKEYBOARDPREF** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de preferencias de teclado.

Además, en Windows 2000, los usuarios pueden establecer un parámetro que indique si las teclas de acceso de los menús siempre están subrayadas. Las aplicaciones usan las marcas **SPI \_ GETMENUUNDERLINES** y **SPI \_ SETMENUUNDERLINES** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro subrayado del menú.

Cuando una aplicación recibe un mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) para el parámetro de preferencia de teclado o de subrayado de menú, se recomienda que la aplicación llame a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para actualizar la información de ambos parámetros.

Tenga en cuenta que **SPI \_ GETMENUUNDERLINES** es el mismo que **SPI \_ GETKEYBOARDCUES** y **SPI \_ SETMENUUNDERLINES** es igual que **SPI \_ SETKEYBOARDCUES**.

 

 