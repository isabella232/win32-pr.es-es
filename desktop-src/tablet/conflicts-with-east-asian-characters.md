---
description: Algunos gestos de la aplicación pueden entrar en conflicto con los caracteres de Asia oriental o con combinaciones de caracteres de Asia oriental.
ms.assetid: 56ff773f-ef95-47f8-ba04-2593330867ee
title: Conflictos con caracteres de East-Asian
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb12b9fab1389395b249f35da3dc5ffbfc91af83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153751"
---
# <a name="conflicts-with-east-asian-characters"></a>Conflictos con caracteres de East-Asian

Algunos *gestos* de la aplicación pueden entrar en conflicto con los caracteres de Asia oriental o con combinaciones de caracteres de Asia oriental. En la tabla siguiente se enumeran los posibles conflictos entre los movimientos de aplicación y los caracteres de las aplicaciones que tienen entradas de caracteres de Asia oriental específicas.



| Gesto                 | Chino (simplificado) | Chino (tradicional) | Japonés     | Coreano       |
|-------------------------|----------------------|-----------------------|--------------|--------------|
| Bajar<br/>         | X<br/>         | X<br/>          | X<br/> | X<br/> |
| Right<br/>        | X<br/>         | X<br/>          | X<br/> | X<br/> |
| DownRight<br/>    | -<br/>         | X<br/>          | -<br/> | X<br/> |
| RightDown<br/>    | -<br/>         | -<br/>          | X<br/> | X<br/> |
| Circle<br/>       | -<br/>         | -<br/>          | -<br/> | X<br/> |
| ChevronRight<br/> | -<br/>         | -<br/>          | -<br/> | X<br/> |



 

Microsoft sigue comprometidos con el desarrollo de *gestos*. Microsoft reconoce que en la creación de aplicaciones, los fabricantes de software independientes (ISV) necesitan saber qué acciones se asignarán a los gestos. [Glifos no implementados](unimplemented-glyphs.md) muestra un conjunto de acciones de lápiz que Microsoft planea asignar a gestos, así como gestos que se reservan para las acciones. Esta información se proporciona para que sepa qué acciones y gestos se proporcionarán en el futuro.

Además de usar gestos que se proporcionan en Microsoft Windows XP Tablet PC Edition, las aplicaciones pueden crear sus propios gestos. Estos gestos pueden ser reconocidos por un *reconocedor de gestos de Microsoft* que el desarrollador de la aplicación compila. Si planea implementar cualquiera de sus propios gestos, consulte [glifos no implementados](unimplemented-glyphs.md) para evitar la superposición con los gestos que Microsoft planea implementar.

 

 




