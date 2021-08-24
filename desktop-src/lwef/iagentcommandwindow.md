---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80509efbe4f9d6391b3ac6ffbdf5cb02580826fd1aa7a94f1536ba5706322606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105191"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

**IAgentCommandWindow define** una interfaz que permite a las aplicaciones establecer y consultar las propiedades de la ventana Comandos de voz. La ventana Comandos de voz es un recurso compartido diseñado principalmente para permitir que los usuarios puedan ver comandos habilitados para voz. Si el reconocimiento de voz está deshabilitado, todavía se muestra la ventana Comandos de voz, con el texto "Entrada de voz deshabilitada" (en el idioma del carácter). Si no hay ningún motor de voz instalado que coincida con la configuración de idioma del carácter, la ventana muestra "Entrada de voz no disponible". Si el cliente activo de entrada no ha definido parámetros de voz para sus comandos y ha deshabilitado los comandos de voz global, la ventana muestra "Sin comandos de voz". También puede consultar las propiedades de la ventana Comandos de voz independientemente de si la entrada de voz está deshabilitada o si está instalado un motor de voz compatible.

**Métodos en orden de Vtable**



| Métodos IAgentCommandWindow                             | Descripción                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | Establece el valor de la [**propiedad Visible**](visible-property.md) de la ventana Comandos de voz.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Devuelve el valor de la [**propiedad Visible**](visible-property.md) de la ventana Comandos de voz. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Devuelve la posición de la ventana Comandos de voz.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Devuelve el tamaño de la ventana Comandos de voz.                                                      |



 

 

 




