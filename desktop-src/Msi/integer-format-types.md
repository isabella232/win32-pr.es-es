---
description: Los tipos de formato entero de los datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato entero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814403"
---
# <a name="integer-format-types"></a>Tipos de formato entero

Los tipos de formato entero de los datos configurables se pueden usar en campos de base de datos de texto o enteros. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.

Existe el siguiente tipo de formato entero.

[Tipo de entero arbitrario](arbitrary-integer-type.md)

Los elementos configurables del tipo de formato entero se utilizan en columnas de texto o de enteros y, en general, se pueden reemplazar por cualquier entero positivo o negativo. Sin embargo, los elementos configurables concretos también pueden tener restricciones semánticas característicos. Por ejemplo, un determinado elemento configurable debe ser un entero entre 0 y 100 y una restricción semántica adicional. Estas restricciones no se aplican mediante Mergemod.dll y, por tanto, los autores de módulos deben estar preparados para controlar cualquier cadena que satisfaga el tipo de formato entero especificado.

 

 



