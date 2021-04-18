---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704709"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

**IAgentCommandWindow** define una interfaz que permite a las aplicaciones establecer y consultar las propiedades de la ventana comandos de voz. La ventana comandos de voz es un recurso compartido diseñado principalmente para permitir a los usuarios ver comandos habilitados para voz. Si el reconocimiento de voz está deshabilitado, se muestra la ventana comandos de voz, con el texto "entrada de voz deshabilitada" (en el idioma del carácter). Si no hay instalado ningún motor de voz que coincida con la configuración de idioma del carácter, la ventana muestra "entrada de voz no disponible". Si el cliente de entrada-activo no ha definido los parámetros de voz para sus comandos y ha deshabilitado los comandos de voz globales, la ventana muestra el mensaje "no hay comandos de voz". También puede consultar las propiedades de la ventana comandos de voz independientemente de si la entrada de voz está deshabilitada o si se ha instalado un motor de voz compatible.

**Métodos en orden de Vtable**



| Métodos IAgentCommandWindow                             | Descripción                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | Establece el valor de la propiedad [**visible**](visible-property.md) de la ventana comandos de voz.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Devuelve el valor de la propiedad [**visible**](visible-property.md) de la ventana comandos de voz. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Devuelve la posición de la ventana comandos de voz.                                                  |
| [**GetSize (**](iagentcommandwindow--getsize.md)         | Devuelve el tamaño de la ventana comandos de voz.                                                      |



 

 

 




