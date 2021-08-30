---
description: Algunos gestos de aplicación pueden estar en conflicto con caracteres de Este de Asia o combinaciones de caracteres de Este de Asia.
ms.assetid: 56ff773f-ef95-47f8-ba04-2593330867ee
title: Conflictos con East-Asian caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171e6401e01bb20bede7f9291d492692c2c11f3bf61ced36a40c300f909e25f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110995"
---
# <a name="conflicts-with-east-asian-characters"></a>Conflictos con East-Asian caracteres

Algunos *gestos de aplicación pueden* estar en conflicto con caracteres de Este de Asia o combinaciones de caracteres de Este de Asia. En la tabla siguiente se enumeran los posibles conflictos entre los gestos de aplicación y los caracteres de las aplicaciones que tienen una entrada de caracteres de Asia Oriental específica.



| Gesto                 | Chino (simplificado) | Chino (tradicional) | Japonés     | Coreano       |
|-------------------------|----------------------|-----------------------|--------------|--------------|
| Bajar<br/>         | X<br/>         | X<br/>          | X<br/> | X<br/> |
| Right<br/>        | X<br/>         | X<br/>          | X<br/> | X<br/> |
| DownRight<br/>    | -<br/>         | X<br/>          | -<br/> | X<br/> |
| RightDown<br/>    | -<br/>         | -<br/>          | X<br/> | X<br/> |
| Circle<br/>       | -<br/>         | -<br/>          | -<br/> | X<br/> |
| ChevronRight<br/> | -<br/>         | -<br/>          | -<br/> | X<br/> |



 

Microsoft sigue comprometido a desarrollar *gestos*. Microsoft reconoce que, al compilar aplicaciones, los proveedores de software independientes (ISV) deben saber qué acciones se asignarán a los gestos. [Glifos sin](unimplemented-glyphs.md) implementar enumera un conjunto de acciones de lápiz que Microsoft planea asignar a gestos, así como gestos que se reservan para acciones. Esta información se proporciona para que sepa para qué acciones y gestos se van a proporcionar en el futuro.

Además de usar gestos que se proporcionan en Microsoft Windows XP Tablet PC Edition, las aplicaciones pueden crear sus propios gestos. Estos gestos pueden ser reconocidos por un reconocedor de gestos de *Microsoft* que el desarrollador de la aplicación compila. Si planea implementar cualquiera de sus propios gestos, consulte Glifos no [implementados](unimplemented-glyphs.md) para evitar que se superpongan los gestos que Microsoft planea implementar.

 

 




