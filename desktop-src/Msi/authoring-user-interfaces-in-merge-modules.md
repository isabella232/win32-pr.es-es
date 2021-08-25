---
description: Los módulos de combinación rara vez requieren una interfaz de usuario.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Creación de interfaces de usuario en módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931e539d8880c490853b20a6e53b3000f390c0b29f81bf8bb9d3e3703e3f7905
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829195"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Creación de interfaces de usuario en módulos de mezcla

Los módulos de combinación rara vez requieren una interfaz de usuario. La publicación de un módulo de combinación que contiene componentes instalables y una interfaz de usuario restringe en última instancia la flexibilidad del usuario del módulo. La combinación de componentes e interfaz de usuario en un módulo puede impedir que los desarrolladores usen su propia interfaz de usuario o proporcionen instalaciones silenciosas. Una alternativa mejor es liberar dos módulos de combinación, uno que instala los componentes de forma silenciosa y un segundo módulo opcional que contiene la interfaz de usuario. El módulo con la interfaz de usuario debe enumerar el módulo de componentes en su [tabla ModuleDependency](moduledependency-table.md). Este método permite a los autores de módulos proporcionar una interfaz de usuario sin forzarla a los desarrolladores.

Cuando se usan tablas de interfaz de usuario en módulos de combinación, se pueden combinar de la misma manera que cualquier otra tabla.

 

 



