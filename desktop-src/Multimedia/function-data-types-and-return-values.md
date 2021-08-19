---
title: Tipos de datos de función y valores devueltos
description: Tipos de datos de función y valores devueltos
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d85ed42a0751147a1a6a61a078ac0899ce0b5756467005fd02ec72d6190096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988320"
---
# <a name="function-data-types-and-return-values"></a>Tipos de datos de función y valores devueltos

Las funciones y macros AVIFile usan controladores de archivos y secuencias implementados con tecnología OLE. El tipo de datos estándar de una función OLE es **STDAPI** y la función devuelve un **valor HRESULT** (cero si se ha producido correctamente o un error en caso contrario). Si una función devuelve un valor distinto de **un valor HRESULT**, el tipo del prototipo de la función tiene una sintaxis ligeramente diferente que inserta el tipo de valor devuelto entre paréntesis después de "STDAPI". \_ Por ejemplo, una función que devuelve un valor de datos **LONG** usa **STDAPI \_ (LONG)** en la instrucción prototype.

 

 




