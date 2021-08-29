---
title: Exponer Owner-Drawn elementos de cuadro combinado
description: Los desarrolladores de aplicaciones no necesitan implementar IAccessible para exponer los elementos de un cuadro combinado dibujado por el propietario que tiene el estilo CBS HASSTRINGS porque Microsoft Active Accessibility expone los elementos en cuadros combinados con este \_ estilo.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fea00a20dc0e6290ee7331a4caabf988558d81e3cc2f56511dfbefbaf1bb0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828947"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Exponer Owner-Drawn elementos de cuadro combinado

Los desarrolladores de aplicaciones no necesitan implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para exponer los elementos de un cuadro combinado dibujado por el propietario que tiene el estilo **CBS \_ HASSTRINGS** porque Microsoft Active Accessibility expone los elementos en cuadros combinados con este estilo. Los elementos de un cuadro combinado dibujado por el propietario con el estilo **\_ HASSTRINGS** de CBS se muestran como texto. Sin embargo, este estilo también se usa con cuadros combinados dibujados por el propietario que no muestran texto para que los elementos del cuadro combinado se exponán mediante Microsoft Active Accessibility.

Para permitir Microsoft Active Accessibility exponer los elementos en un cuadro combinado dibujado por el propietario que no muestra texto:

-   Use el **estilo \_ HASSTRINGS de CBS** al crear el cuadro combinado.
-   Cree un homólogo textual que nombre o describa cada elemento del cuadro combinado.
-   Al agregar elementos al cuadro combinado dibujado por el propietario, use el mensaje CB ADDSTRING para agregar el texto que \_ Microsoft Active Accessibility exponer. Este texto no se muestra, por lo que no debe formar parte de los datos dibujados por el propietario. Agregue los datos del elemento dibujado por el propietario mediante el \_ mensaje CB SETITEMDATA.

Al usar el método anterior, tenga en cuenta lo siguiente:

-   Si usa el estilo SORT de **CBS, \_** el cuadro combinado se ordena mediante las cadenas proporcionadas y no el procedimiento de devolución de llamada [ \_ COMPAREITEM](../controls/wm-compareitem.md) de WM.
-   Con los cuadros combinados de variables dibujadas por el propietario creados con el estilo **CBS \_ OWNERDRAWVARIABLE**, use una variable global o algún otro mecanismo para realizar un seguimiento de cuándo es válido el miembro **itemData** de [MEASUREITEMSTRUCT.](/windows/win32/api/winuser/ns-winuser-measureitemstruct) La variable global es necesaria porque el sistema envía el mensaje [ \_ WM MEASUREITEM](../controls/wm-measureitem.md) en cuanto se agrega la cadena, pero antes de adjuntar los datos del elemento y, en este momento, el miembro **itemData** no es válido.
-   Para cambiar la cadena de un elemento en un cuadro combinado con el estilo **\_ HASSTRINGS de CBS,** elimine el elemento con el mensaje [ \_ DELETESTRING](../controls/cb-deletestring.md) de CB y agregue la nueva cadena con el mensaje [ \_ ADDSTRING de CB.](../controls/cb-addstring.md)

 

 