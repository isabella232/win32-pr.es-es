---
title: Elección de las propiedades que se admitirán
description: Las propiedades IAccessible proporcionan una manera para que los desarrolladores de servidores describan una amplia variedad de elementos de la interfaz de usuario.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466127"
---
# <a name="choosing-which-properties-to-support"></a>Elección de las propiedades que se admitirán

Las [**propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan una manera para que los desarrolladores de servidores describan una amplia variedad de elementos de la interfaz de usuario. Pero no todas las propiedades son aplicables a todos los tipos de elemento de interfaz de usuario. Además, algunas propiedades proporcionan información descriptiva que es útil, pero no esencial.

Los servidores deben admitir las siguientes propiedades y métodos para cada objeto:

-   [**Nombre**](name-property.md)
-   [**Role**](role-property.md)
-   [**State**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Las siguientes propiedades y métodos deben ser compatibles si son aplicables al objeto :

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Value**](value-property.md)

Las siguientes propiedades y métodos deben ser compatibles si el objeto tiene elementos secundarios:

-   [**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) y [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Focus, Selection**](selection-and-focus-properties-and-methods.md)e [ **IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Las siguientes propiedades son opcionales, pero proporcionan información descriptiva útil sobre el objeto . La [**propiedad Description**](description-property.md) se implementa para describir mapas de bits y otras imágenes.

-   [**Descripción**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) e [ **IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Ayuda**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 




