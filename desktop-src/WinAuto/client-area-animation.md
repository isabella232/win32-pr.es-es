---
title: Parámetro de animación de área de cliente
description: La marca de animación del área de cliente indica si el usuario desea deshabilitar las animaciones en los elementos de la interfaz de usuario.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4d451424da0a02fa55efaead05ab285b3f07936167bb6e4376de4fd25ae11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325964"
---
# <a name="client-area-animation-parameter"></a>Parámetro de animación de área de cliente

El parámetro de animación de área de cliente indica si el usuario desea deshabilitar las animaciones en los elementos de la interfaz de usuario. Mostrar características como parpadear, parpadear, parpadear y mover contenido puede provocar daños en los usuarios con sensibilidad a la foto. Este parámetro permite habilitar o deshabilitar todas estas animaciones.

Las aplicaciones usan las marcas **SPI \_ GETCLIENTAREAANIMATION** y **SPI \_ SETCLIENTAREAANIMATION** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para activar o desactivar las animaciones de área de cliente.

 

 