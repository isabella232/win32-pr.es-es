---
title: Tipos de datos de función y valores devueltos
description: Tipos de datos de función y valores devueltos
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994148"
---
# <a name="function-data-types-and-return-values"></a>Tipos de datos de función y valores devueltos

Las funciones y macros de AVIFile utilizan controladores de archivos y secuencias implementados con la tecnología OLE. El tipo de datos estándar de una función OLE es **STDAPI** y la función devuelve un valor **HRESULT** (cero si es correcto o un error de lo contrario). Si una función devuelve un valor distinto de **HRESULT**, el tipo del prototipo de la función tiene una sintaxis ligeramente diferente que incrusta el tipo de valor devuelto entre paréntesis después de "STDAPI \_ ". Por ejemplo, una función que devuelve un valor de datos **Long** usa **STDAPI \_ (Long)** en la instrucción prototype.

 

 




