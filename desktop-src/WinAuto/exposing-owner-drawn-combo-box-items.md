---
title: Exponer Owner-Drawn elementos del cuadro combinado
description: Los desarrolladores de aplicaciones no necesitan implementar IAccessible para exponer los elementos de un cuadro combinado dibujado por el propietario que tenga el estilo CBS \_ HASSTRINGS porque Microsoft Active Accessibility expone los elementos de los cuadros combinados con este estilo.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676455"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Exponer Owner-Drawn elementos del cuadro combinado

Los desarrolladores de aplicaciones no necesitan implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para exponer los elementos de un cuadro combinado dibujado por el propietario que tenga el estilo **CBS \_ HASSTRINGS** porque Microsoft Active Accessibility expone los elementos de los cuadros combinados con este estilo. Los elementos de un cuadro combinado dibujado por el propietario con el estilo **CBS \_ HASSTRINGS** se muestran como texto. Sin embargo, este estilo también se utiliza con cuadros combinados dibujados por el propietario que no muestran texto para que Microsoft Active Accessibility exponga los elementos del cuadro combinado.

Para permitir que Microsoft Active Accessibility exponga los elementos de un cuadro combinado dibujado por el propietario que no muestre texto:

-   Use el **estilo \_ HASSTRINGS de CBS** al crear el cuadro combinado.
-   Cree un homólogo textual que nombra o describe cada elemento del cuadro combinado.
-   Al agregar elementos al cuadro combinado dibujado por el propietario, use el \_ mensaje CB ADDSTRING para agregar el texto que desea que Microsoft Active Accessibility exponga. Este texto no se muestra, por lo que no debe formar parte de los datos dibujados por el propietario. Agregue los datos del elemento dibujado por el propietario mediante el \_ mensaje CB SETITEMDATA.

Al usar el método anterior, tenga en cuenta lo siguiente:

-   Si usa el estilo **de \_ ordenación CBS** , el cuadro combinado se ordena con las cadenas proporcionadas y no con el procedimiento de devolución de llamada [ \_ COMPAREITEM de WM](../controls/wm-compareitem.md) .
-   Con los cuadros combinados de variables dibujadas por el propietario creados con el estilo **CBS \_ OWNERDRAWVARIABLE**, use una variable global o algún otro mecanismo para realizar un seguimiento de Cuándo es válido el miembro de **itemData** de [measureitemstruct (](/windows/win32/api/winuser/ns-winuser-measureitemstruct) . La variable global es necesaria porque el sistema envía el mensaje de [WM \_ MEASUREITEM](../controls/wm-measureitem.md) en cuanto se agrega la cadena, pero antes de que se adjunten los datos del elemento, y en este momento el miembro de **itemData** no es válido.
-   Para cambiar la cadena de un elemento en un cuadro combinado con el estilo **CBS \_ HASSTRINGS** , elimine el elemento con el mensaje [CB \_ DELETESTRING](../controls/cb-deletestring.md) y agregue la nueva cadena con el mensaje [CB \_ ADDSTRING](../controls/cb-addstring.md) .

 

 