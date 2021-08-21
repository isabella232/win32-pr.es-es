---
title: Atributo TableLimits de VML
description: Atributo TableLimits de VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af52ba570b04e56f1dede169045f7ee1addf374fae5ca4f1cd5de4d9390f1235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959255"
---
# <a name="vml-tablelimits-attribute"></a>Atributo TableLimits de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Lista de valores de alto mínimo para cada fila de una tabla. Lectura/escritura **DvLengthArray**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* o:tablelimits=" *expression* ">

**Comentarios:**

Usado por Microsoft PowerPoint tablas nativas. El valor predeterminado es **Null.**

Aunque el valor se almacena en una forma, el atributo solo es útil cuando la tabla está creada por formas agrupadas. Cuando se agrega texto a las celdas de la tabla, el alto de la fila puede aumentar. El **atributo TableLimits** almacena el alto de fila original para que, si se elimina el texto, el alto de la fila no se encuentra por debajo del valor original.

*Microsoft Office Atributo Extensions*

 

 