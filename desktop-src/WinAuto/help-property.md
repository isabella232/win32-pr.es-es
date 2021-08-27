---
title: Propiedad Help
description: La propiedad Help proporciona información que indica al usuario sobre la función de un objeto .
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6f8b226c483e3a3d68f878fccb940fc1a9f69f18b6fde62eed4b5a7a8ea9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122195"
---
# <a name="help-property"></a>Propiedad Help

La **propiedad** Help proporciona información que indica al usuario sobre la función de un objeto .

La **propiedad Help** se recupera mediante una llamada a [**IAccessible::get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Esta propiedad contiene información de estilo globo (como se encuentra en información sobre herramientas) que se usa para describir lo que hace el objeto o cómo usarlo. Por ejemplo, la **propiedad Ayuda** de un botón de la barra de herramientas que muestra una impresora podría proporcionar el texto siguiente: "Imprime el documento actual".

El texto de la **propiedad Ayuda** no tiene que ser único dentro de la interfaz de usuario.

## <a name="when-to-support-the-help-property"></a>Cuándo admitir la propiedad de Ayuda

Los servidores no admiten la **propiedad Ayuda** si otras propiedades proporcionan información suficiente sobre el propósito del objeto y las acciones que realiza el objeto. Los objetos accesibles que exponen controles proporcionados por el sistema no admiten la **propiedad Ayuda.**

 

 




