---
title: El objeto CommandsWindow
description: El objeto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714352"
---
# <a name="the-commandswindow-object"></a>El objeto CommandsWindow

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) proporciona acceso a las propiedades de la ventana comandos de voz. La ventana comandos de voz es un recurso compartido diseñado principalmente para permitir a los usuarios ver comandos habilitados para voz. Si el reconocimiento de voz está deshabilitado, se muestra la ventana comandos de voz, con el texto "entrada de voz deshabilitada" (en el idioma del carácter). Si no hay instalado ningún motor de voz que coincida con la configuración de idioma del carácter, se muestra "entrada de voz no disponible". Si el cliente de entrada-activo no ha definido los parámetros de voz para sus comandos y ha deshabilitado los comandos de voz globales, la ventana muestra el mensaje "no hay comandos de voz". También puede consultar las propiedades de la ventana comandos de voz independientemente de si la entrada de voz está deshabilitada o si se ha instalado un motor de voz compatible.

-   [Propiedades de CommandsWindow](commandswindow-properties.md)

 

 