---
description: Los módulos de combinación raramente requieren una interfaz de usuario.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Crear interfaces de usuario en módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667025"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Crear interfaces de usuario en módulos de combinación

Los módulos de combinación raramente requieren una interfaz de usuario. La liberación de un módulo de combinación que contenga componentes instalables y una interfaz de usuario restringe en última instancia la flexibilidad del usuario del módulo. La combinación de los componentes y la interfaz de usuario en un módulo puede impedir que los desarrolladores usen su propia interfaz de usuario o que proporcionen instalaciones silenciosas. Una alternativa mejor es liberar dos módulos de combinación, uno que instala silenciosamente los componentes y un segundo módulo opcional que contiene la interfaz de usuario. El módulo con la interfaz de usuario debe mostrar el módulo de componentes en la [tabla ModuleDependency](moduledependency-table.md). Este método permite a los autores de módulos proporcionar una interfaz de usuario sin forzarla a los desarrolladores.

Cuando las tablas de la interfaz de usuario se utilizan en módulos de combinación, se pueden combinar de la misma manera que cualquier otra tabla.

 

 



