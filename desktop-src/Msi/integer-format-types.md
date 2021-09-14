---
description: Los tipos de formato entero de datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato entero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072018"
---
# <a name="integer-format-types"></a>Tipos de formato entero

Los tipos de formato entero de datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.

Existe el siguiente tipo de formato entero.

[Tipo entero arbitrario](arbitrary-integer-type.md)

Los elementos configurables del tipo de formato entero se usan en columnas de texto o entero y, en general, podrían reemplazarse por cualquier entero positivo o negativo. Sin embargo, determinados elementos configurables también pueden tener restricciones semánticas características. Por ejemplo, un elemento configurable determinado que debe ser un entero entre 0 y 100 tiene una restricción semántica adicional. Estas restricciones no se aplican mediante Mergemod.dll, por lo que los autores de módulos deben estar preparados para controlar cualquier cadena que satisfaga el tipo de formato entero especificado.

 

 



