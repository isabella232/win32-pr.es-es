---
description: Los tipos de formato de texto de los datos configurables pueden ser cadenas de texto de cualquier longitud. No se permiten valores NULL incrustados.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipos de formato de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a77ef5e6948320deba8df992e2cf9447cbda82d6a20fc4329f97e761f425164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626335"
---
# <a name="text-format-types"></a>Tipos de formato de texto

Los tipos de formato de texto de los datos configurables pueden ser cadenas de texto de cualquier longitud. No se permiten valores NULL incrustados.

Existen los siguientes tipos de formato de texto:

[Texto arbitrario](arbitrary-text-type.md)

[Rtf](rtf-type.md)

[Formato](formatted-type.md)

[Enum](enum-type.md)

[Tipo de identificador](identifier-type.md)

Los elementos configurables del tipo de formato de texto se usan en campos de base de datos no binarios y, en general, podrían reemplazarse por cualquier cadena de cualquier longitud. Sin embargo, determinados elementos configurables también tienen restricciones semánticas. Por ejemplo, un elemento configurable que debe ser una clave externa en una tabla específica tiene restricciones semánticas adicionales. Estas restricciones semánticas no se aplican por Mergemod.dll y, por lo tanto, los autores de módulos deben estar preparados para controlar cualquier cadena que satisfaga el tipo de formato de texto especificado.

 

 



