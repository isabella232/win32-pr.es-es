---
title: Parámetro de preferencia de teclado
description: El parámetro de preferencia de teclado indica que el usuario se basa en el teclado en lugar del mouse, por lo que las aplicaciones deben mostrar interfaces de teclado que, de lo contrario, se ocultarían.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070698"
---
# <a name="keyboard-preference-parameter"></a>Parámetro de preferencia de teclado

El parámetro de preferencia de teclado indica que el usuario se basa en el teclado en lugar del mouse, por lo que las aplicaciones deben mostrar interfaces de teclado que, de lo contrario, se ocultarían.

El usuario controla la configuración del parámetro de preferencia de teclado mediante el Centro de accesibilidad en Panel de control u otra aplicación para personalizar el entorno. Las aplicaciones usan las marcas **SPI \_ GETKEYBOARDPREF** y **SPI \_ SETKEYBOARDPREF** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de preferencia de teclado.

Además, en Windows 2000, los usuarios pueden establecer un parámetro que indica si las teclas de acceso al menú siempre están subrayadas. Las aplicaciones usan las marcas **\_ SPI GETMENUUNDERLINES** y **SPI \_ SETMENUUNDERLINES** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro underlines del menú.

Cuando una aplicación recibe un mensaje [**\_ WM SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) para la preferencia de teclado o el parámetro de subrayado de menú, se recomienda que la aplicación llame a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para actualizar la información de ambos parámetros.

Tenga en cuenta que **SPI \_ GETMENUUNDERLINES** es el mismo que **SPI \_ GETKEYBOARDCUES** y **SPI \_ SETMENUUNDERLINES** es el mismo que **SPI \_ SETKEYBOARDCUES.**

 

 