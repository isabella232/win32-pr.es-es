---
title: Exponer Owner-Drawn de cuadro combinado
description: Los desarrolladores de aplicaciones no necesitan implementar IAccessible para exponer los elementos de un cuadro combinado dibujado por el propietario que tiene el estilo CBS HASSTRINGS porque Microsoft Active Accessibility expone los elementos en cuadros combinados con este \_ estilo.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160569"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Exponer Owner-Drawn de cuadro combinado

Los desarrolladores de aplicaciones no necesitan implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para exponer los elementos de un cuadro combinado dibujado por el propietario que tiene el estilo **CBS \_ HASSTRINGS** porque Microsoft Active Accessibility expone los elementos en cuadros combinados con este estilo. Los elementos de un cuadro combinado dibujado por el propietario con el estilo **\_ HASSTRINGS** de CBS se muestran como texto. Sin embargo, este estilo también se usa con cuadros combinados dibujados por el propietario que no muestran texto para que los elementos del cuadro combinado se exponán mediante Microsoft Active Accessibility.

Para permitir Microsoft Active Accessibility exponer los elementos en un cuadro combinado dibujado por el propietario que no muestra texto:

-   Use el **estilo \_ HASSTRINGS de CBS** al crear el cuadro combinado.
-   Cree un homólogo textual que nombre o describa cada elemento del cuadro combinado.
-   Al agregar elementos al cuadro combinado dibujado por el propietario, use el mensaje CB ADDSTRING para agregar el texto que \_ Microsoft Active Accessibility exponer. Este texto no se muestra, por lo que no debe formar parte de los datos dibujados por el propietario. Agregue los datos del elemento dibujado por el propietario mediante el \_ mensaje CB SETITEMDATA.

Al usar el método anterior, tenga en cuenta lo siguiente:

-   Si usa el estilo SORT de **CBS, \_** el cuadro combinado se ordena mediante las cadenas proporcionadas y no el procedimiento de devolución de llamada [ \_ COMPAREITEM](../controls/wm-compareitem.md) de WM.
-   Con los cuadros combinados de variables dibujadas por el propietario creados con el estilo **CBS \_ OWNERDRAWVARIABLE**, use una variable global o algún otro mecanismo para realizar un seguimiento de cuándo es válido el miembro **itemData** de [MEASUREITEMSTRUCT.](/windows/win32/api/winuser/ns-winuser-measureitemstruct) La variable global es necesaria porque el sistema envía el mensaje [ \_ WM MEASUREITEM](../controls/wm-measureitem.md) en cuanto se agrega la cadena, pero antes de adjuntar los datos del elemento y, en este momento, el miembro **itemData** no es válido.
-   Para cambiar la cadena de un elemento en un cuadro combinado con el estilo **\_ HASSTRINGS de CBS,** elimine el elemento con el mensaje [ \_ DELETESTRING](../controls/cb-deletestring.md) de CB y agregue la nueva cadena con el mensaje [ \_ ADDSTRING de CB.](../controls/cb-addstring.md)

 

 