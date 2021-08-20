---
title: Atributo print de VML
description: Atributo print de VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfa364e573d887da2013f946ddf23e0a974e0f63211623de3d2046b0525b2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057733"
---
# <a name="vml-print-attribute"></a>Atributo print de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se imprimirá la forma. Lectura/escritura [DvTriState](msdn-online-vml-vgtristate.md).

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* print=" *expression* ">

**Sintaxis de script**

*element* .print="*expression*"

*expresión* = *elemento*.print

**Comentarios:**

Se proporciona como una manera de especificar si se imprimirán las formas. Tenga en cuenta que una forma todavía se puede mostrar en la pantalla, incluso si no se imprime como resultado de que este atributo sea **False.** El valor predeterminado es **True**.

Este atributo lo usa Microsoft Office, pero no lo usa Microsoft Internet Explorer.

*Microsoft Office Atributo Extensions*

 

 