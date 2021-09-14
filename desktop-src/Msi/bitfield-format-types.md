---
description: Los tipos de formato de campo de bits de datos configurables se pueden usar en campos de base de datos enteros.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Tipos de formato de campo de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b443f7ee363d1a2b48eb580623018264df8d50be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158972"
---
# <a name="bitfield-format-types"></a>Tipos de formato de campo de bits

Los tipos de formato de campo de bits de datos configurables se pueden usar en campos de base de datos enteros. El usuario debe elegir un valor de un subconjunto especificado. Esto es solo por convención y no se aplica mediante Mergemod.dll. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo.

Existe el siguiente tipo de formato de campo de bits.

[Tipo de campo de bits arbitrario](arbitrary-bitfield-type.md)

Los elementos configurables del tipo de formato de campo de bits se usan en columnas de enteros y, en general, podrían reemplazarse por cualquier entero. El usuario debe elegir un valor de un subconjunto especificado. Sin embargo, esto es solo por convención y no se aplica mediante Mergemod.dll. El autor debe preparar el módulo para controlar cualquier valor.

 

 



