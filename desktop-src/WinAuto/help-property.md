---
title: Propiedad Help
description: La propiedad Ayuda proporciona información que indica al usuario sobre la función de un objeto .
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160562"
---
# <a name="help-property"></a>Propiedad Help

La **propiedad** Ayuda proporciona información que indica al usuario sobre la función de un objeto .

La **propiedad** Help se recupera mediante una llamada a [**IAccessible::get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Esta propiedad contiene información de estilo globo (como se encuentra en Información sobre herramientas) que se usa para describir lo que hace el objeto o cómo usarlo. Por ejemplo, la **propiedad Ayuda** de un botón de la barra de herramientas que muestra una impresora podría proporcionar el texto siguiente: "Imprime el documento actual".

El texto de la **propiedad Ayuda** no tiene que ser único dentro de la interfaz de usuario.

## <a name="when-to-support-the-help-property"></a>Cuándo se debe admitir la propiedad Ayuda

Los servidores no admiten la **propiedad Ayuda** si otras propiedades proporcionan información suficiente sobre el propósito del objeto y las acciones que realiza el objeto. Los objetos accesibles que exponen controles proporcionados por el sistema no admiten la **propiedad Ayuda.**

 

 




