---
title: Atributo InvX de VML
description: Atributo InvX de VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e040c4ff013ec9c2a606e1034458f9149d666813dd42341d9ec68a39901094b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600131"
---
# <a name="vml-invx-attribute"></a>Atributo InvX de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se invierte la posición x del identificador. Lectura/escritura **DvTriState**.

**Se aplica a**

[H](msdn-online-vml-h-element.md) (subelemento de [identificadores)](msdn-online-vml-handles-element.md)

**Sintaxis de etiquetas**

<v: *element* invx=" *expression* ">

**Comentarios:**

Si **es True**, la posición x del identificador se invierte restando el valor x del valor x de **CoordOrigin** agregado al valor x de **CoordSize**. El valor predeterminado es **False**.

Este atributo es el equivalente de

coordorigin.x + coordsize.x - h.position.x

*Atributo estándar de VML*

 

 