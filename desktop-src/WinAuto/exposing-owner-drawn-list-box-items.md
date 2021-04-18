---
title: Exponer Owner-Drawn elementos del cuadro de lista
description: Los desarrolladores de aplicaciones no necesitan implementar IAccessible para exponer los elementos de un cuadro de lista dibujado por el propietario que tenga el estilo LBS \_ HASSTRINGS porque Microsoft Active Accessibility expone los elementos de los cuadros de lista con este estilo.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbb72285f55796a285cd6e1a8838a629218659b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421175"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Exponer Owner-Drawn elementos del cuadro de lista

Los desarrolladores de aplicaciones no necesitan implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para exponer los elementos de un cuadro de lista dibujado por el propietario que tenga el estilo **lbs \_ HASSTRINGS** porque Microsoft Active Accessibility expone los elementos de los cuadros de lista con este estilo. Los elementos de un cuadro de lista dibujado por el propietario con el estilo **lb \_ HASSTRINGS** se muestran como texto. Sin embargo, este estilo también se utiliza con cuadros de lista dibujados por el propietario que no muestran texto para que Microsoft Active Accessibility exponga los elementos del cuadro de lista.

Para permitir que Microsoft Active Accessibility exponga los elementos de un cuadro de lista dibujado por el propietario que no muestre texto:

-   Use el estilo **lbs \_ HASSTRINGS** al crear el cuadro de lista.
-   Cree un homólogo textual que nombra o describe cada elemento en el cuadro de lista.
-   Al agregar elementos al cuadro de lista dibujado por el propietario, use [el \_ mensaje de lb en lb](../controls/lb-addstring.md) para agregar el texto que desea que Microsoft Active Accessibility exponga. Este texto no se muestra, por lo que no forma parte de los datos dibujados por el propietario. Agregue los datos del elemento dibujado por el propietario mediante el mensaje [lb \_ SETITEMDATA](../controls/lb-setitemdata.md) .

Al usar el método anterior, tenga en cuenta lo siguiente:

-   Si usa el estilo **de \_ ordenación lbs** , el cuadro de lista se ordena utilizando las cadenas proporcionadas y no el procedimiento de devolución de llamada [ \_ COMPAREITEM de WM](../controls/wm-compareitem.md) .
-   Con los cuadros de lista de variables dibujadas por el propietario creados con el estilo **lbs \_ OWNERDRAWVARIABLE**, use una variable global o algún otro mecanismo para realizar un seguimiento de Cuándo es válido el **miembro de itemData** de [measureitemstruct (](/windows/win32/api/winuser/ns-winuser-measureitemstruct) . La variable global es necesaria porque el sistema envía el mensaje de [WM \_ MEASUREITEM](../controls/wm-measureitem.md) en cuanto se agrega la cadena, pero antes de que se adjunten los datos del elemento, y en este momento el miembro de **itemData** no es válido.
-   Para cambiar la cadena de un elemento en un cuadro de lista con el estilo **lb \_ HASSTRINGS** , elimine el elemento con el mensaje [lb \_ DELETESTRING](../controls/lb-deletestring.md) y agregue la nueva cadena con el mensaje de lb en lb \_ .

 

 