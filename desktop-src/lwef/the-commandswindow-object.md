---
title: El objeto CommandsWindow
description: El objeto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336bdff598a75a9b0b07adabb11c271a45ca84940f528ebe082de17841592d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882469"
---
# <a name="the-commandswindow-object"></a>El objeto CommandsWindow

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El [**objeto CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) proporciona acceso a las propiedades de la ventana Comandos de voz. La ventana Comandos de voz es un recurso compartido diseñado principalmente para permitir que los usuarios puedan ver comandos habilitados para voz. Si el reconocimiento de voz está deshabilitado, todavía se muestra la ventana Comandos de voz, con el texto "Entrada de voz deshabilitada" (en el idioma del carácter). Si no se instala ningún motor de voz que coincida con la configuración del idioma del carácter, se muestra la ventana "Entrada de voz no disponible". Si el cliente activo de entrada no ha definido parámetros de voz para sus comandos y ha deshabilitado los comandos de voz global, la ventana muestra "Sin comandos de voz". También puede consultar las propiedades de la ventana Comandos de voz independientemente de si la entrada de voz está deshabilitada o si está instalado un motor de voz compatible.

-   [Comandos Propiedades de Windows](commandswindow-properties.md)

 

 