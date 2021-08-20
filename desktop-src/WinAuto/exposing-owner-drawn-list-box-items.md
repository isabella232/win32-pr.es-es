---
title: Exponer Owner-Drawn de cuadro de lista
description: Los desarrolladores de aplicaciones no necesitan implementar IAccessible para exponer los elementos de un cuadro de lista dibujado por el propietario que tiene el estilo LBS HASSTRINGS porque Microsoft Active Accessibility expone los elementos de los cuadros de lista con este \_ estilo.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fed68477680376373da6c16f59b3fb556b6a435f15f04daae8f3f1262829dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115278"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Exponer Owner-Drawn de cuadro de lista

Los desarrolladores de aplicaciones no necesitan implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para exponer los elementos de un cuadro de lista dibujado por el propietario que tiene el estilo **LBS \_ HASSTRINGS** porque Microsoft Active Accessibility expone los elementos de los cuadros de lista con este estilo. Los elementos de un cuadro de lista dibujado por el propietario con el estilo **\_ HASSTRINGS** de LBS se muestran como texto. Sin embargo, este estilo también se usa con cuadros de lista dibujados por el propietario que no muestran texto para que los elementos del cuadro de lista se exponán mediante Microsoft Active Accessibility.

Para permitir Microsoft Active Accessibility exponer los elementos en un cuadro de lista dibujado por el propietario que no muestra texto:

-   Use el **estilo \_ HASSTRINGS de LBS** al crear el cuadro de lista.
-   Cree un homólogo textual que nombre o describa cada elemento del cuadro de lista.
-   Al agregar elementos al cuadro de lista dibujado por el propietario, use el mensaje [ \_ ADDSTRING](../controls/lb-addstring.md) de LB para agregar el texto que Microsoft Active Accessibility exponer. Este texto no se muestra, por lo que no forma parte de los datos dibujados por el propietario. Agregue los datos del elemento dibujado por el propietario mediante [el \_ mensaje SETITEMDATA de](../controls/lb-setitemdata.md) LB.

Al usar el método anterior, tenga en cuenta lo siguiente:

-   Si usa el estilo **\_ SORT de LBS,** el cuadro de lista se ordena mediante las cadenas proporcionadas y no el procedimiento de devolución de llamada [ \_ COMPAREITEM](../controls/wm-compareitem.md) de WM.
-   Con los cuadros de lista de variables dibujadas por el propietario creados con el estilo **LBS \_ OWNERDRAWVARIABLE**, use una variable global o algún otro mecanismo para realizar un seguimiento de cuándo es válido el miembro **itemData** de [MEASUREITEMSTRUCT.](/windows/win32/api/winuser/ns-winuser-measureitemstruct) La variable global es necesaria porque el sistema envía el mensaje [ \_ WM MEASUREITEM](../controls/wm-measureitem.md) en cuanto se agrega la cadena, pero antes de adjuntar los datos del elemento y, en este momento, el miembro **itemData** no es válido.
-   Para cambiar la cadena de un elemento en un cuadro de lista con el estilo **\_ LB HASSTRINGS,** elimine el elemento con el mensaje [LB \_ DELETESTRING](../controls/lb-deletestring.md) y agregue la nueva cadena con el mensaje \_ LB ADDSTRING.

 

 