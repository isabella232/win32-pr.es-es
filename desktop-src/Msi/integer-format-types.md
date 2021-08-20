---
description: Los tipos de formato entero de datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato entero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf5d4ad0d7ef9ba8adb1ddb919e284dbd2a10b2eafc7c43f72d6d0ee777f743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805633"
---
# <a name="integer-format-types"></a>Tipos de formato entero

Los tipos de formato entero de datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.

Existe el siguiente tipo de formato entero.

[Tipo entero arbitrario](arbitrary-integer-type.md)

Los elementos configurables del tipo de formato entero se usan en columnas de texto o entero y, en general, podrían reemplazarse por cualquier entero positivo o negativo. Sin embargo, determinados elementos configurables también pueden tener restricciones semánticas de características. Por ejemplo, un elemento configurable determinado que debe ser un entero entre 0 y 100 tiene una restricción semántica adicional. Estas restricciones no se aplican mediante Mergemod.dll, por lo que los autores de módulos deben estar preparados para controlar cualquier cadena que cumpla el tipo de formato entero especificado.

 

 



