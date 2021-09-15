---
title: Exposición de Owner-Drawn de cuadro de lista
description: Los desarrolladores de aplicaciones no necesitan implementar IAccessible para exponer los elementos de un cuadro de lista dibujado por el propietario que tiene el estilo LBS HASSTRINGS porque Microsoft Active Accessibility expone los elementos de los cuadros de lista con este \_ estilo.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbb72285f55796a285cd6e1a8838a629218659b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474543"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Exposición de Owner-Drawn de cuadro de lista

Los desarrolladores de aplicaciones no necesitan implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para exponer los elementos de un cuadro de lista dibujado por el propietario que tiene el estilo **LBS \_ HASSTRINGS** porque Microsoft Active Accessibility expone los elementos de los cuadros de lista con este estilo. Los elementos de un cuadro de lista dibujado por el propietario con el estilo **\_ HASSTRINGS** de LBS se muestran como texto. Sin embargo, este estilo también se usa con cuadros de lista dibujados por el propietario que no muestran texto para que los elementos del cuadro de lista se exponán mediante Microsoft Active Accessibility.

Para permitir Microsoft Active Accessibility los elementos de un cuadro de lista dibujado por el propietario que no muestra texto:

-   Use el **estilo \_ HASSTRINGS de LBS** al crear el cuadro de lista.
-   Cree un homólogo textual que nombre o describa cada elemento del cuadro de lista.
-   Al agregar elementos al cuadro de lista dibujado por el propietario, use el mensaje [ \_ LB ADDSTRING](../controls/lb-addstring.md) para agregar el texto que Microsoft Active Accessibility exponer. Este texto no se muestra, por lo que no forma parte de los datos dibujados por el propietario. Agregue los datos del elemento dibujado por el propietario mediante [el \_ mensaje LB SETITEMDATA.](../controls/lb-setitemdata.md)

Al usar el método anterior, tenga en cuenta lo siguiente:

-   Si usa el estilo **\_ SORT de LBS,** el cuadro de lista se ordena con las cadenas proporcionadas y no con el procedimiento de devolución de llamada [ \_ COMPAREITEM](../controls/wm-compareitem.md) de WM.
-   Con los cuadros de lista de variables dibujadas por el propietario creados con el estilo **LBS \_ OWNERDRAWVARIABLE**, use una variable global o algún otro mecanismo para realizar un seguimiento de cuándo es válido el miembro **itemData** de [MEASUREITEMSTRUCT.](/windows/win32/api/winuser/ns-winuser-measureitemstruct) La variable global es necesaria porque el sistema envía el mensaje [ \_ WM MEASUREITEM](../controls/wm-measureitem.md) en cuanto se agrega la cadena, pero antes de adjuntar los datos del elemento y, en este momento, el miembro **itemData** no es válido.
-   Para cambiar la cadena de un elemento en un cuadro de lista con el estilo **\_ HASSTRINGS** de LB, elimine el elemento con el mensaje [LB \_ DELETESTRING](../controls/lb-deletestring.md) y agregue la nueva cadena con el mensaje \_ LB ADDSTRING.

 

 