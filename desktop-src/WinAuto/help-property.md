---
title: Propiedad Help
description: La propiedad Help proporciona información que indica al usuario sobre la función de un objeto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357034"
---
# <a name="help-property"></a>Propiedad Help

La propiedad **Help** proporciona información que indica al usuario sobre la función de un objeto.

La propiedad **Help** se recupera llamando a [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Esta propiedad contiene información de estilo de globo (como se encuentra en la información sobre herramientas) que se usa para describir lo que hace el objeto o cómo utilizarlo. Por ejemplo, la propiedad **ayuda** de un botón de la barra de herramientas que muestra una impresora puede proporcionar el texto siguiente: "imprime el documento actual".

No es necesario que el texto de la propiedad de **ayuda** sea único dentro de la interfaz de usuario.

## <a name="when-to-support-the-help-property"></a>Cuándo se debe admitir la propiedad Help

Los servidores no admiten la propiedad **Help** si otras propiedades proporcionan información suficiente sobre el propósito del objeto y las acciones que realiza el objeto. Los objetos accesibles que exponen controles proporcionados por el sistema no admiten la propiedad **Help** .

 

 




