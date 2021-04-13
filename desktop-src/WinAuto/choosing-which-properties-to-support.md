---
title: Elección de las propiedades que se van a admitir
description: Las propiedades IAccessible proporcionan una manera para que los desarrolladores de servidores describan una amplia variedad de elementos de la interfaz de usuario.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357333"
---
# <a name="choosing-which-properties-to-support"></a>Elección de las propiedades que se van a admitir

Las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan una manera para que los desarrolladores de servidores describan una amplia variedad de elementos de la interfaz de usuario. Pero no todas las propiedades se aplican a cada tipo de elemento de la interfaz de usuario. Además, algunas propiedades proporcionan información descriptiva que es útil, pero no esencial.

Los servidores deben admitir los siguientes métodos y propiedades para todos los objetos:

-   [**Name**](name-property.md)
-   [**Role**](role-property.md)
-   [**State**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) y [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) y [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Se deben admitir las siguientes propiedades y métodos si son aplicables al objeto:

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Value**](value-property.md)

Se deben admitir las siguientes propiedades y métodos si el objeto tiene elementos secundarios:

-   [**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) y [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Focus, Selection**](selection-and-focus-properties-and-methods.md)y [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Las siguientes propiedades son opcionales, pero proporcionan información descriptiva útil sobre el objeto. La propiedad [**Description**](description-property.md) se implementa para describir mapas de bits y otras imágenes.

-   [**Descripción**](description-property.md)
-   [**DEFAULTACTION**](defaultaction-property.md) y [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Ayuda**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 




