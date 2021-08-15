---
description: El Conectar del objeto Merge se puede usar para conectar un módulo a una característica adicional que se ha combinado en la base de datos o que se combinará en la base de datos. La característica debe existir antes de llamar a este método.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Conectar un módulo de mezcla a varias características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12044ff293d825c160533907d625a2d12bb9ea217233c54dd9d5a0099990ee3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948426"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Conectar un módulo de mezcla a varias características

El [**Conectar**](merge-connect.md) del objeto [Merge](merge-object.md) se puede usar para conectar un módulo a una característica adicional que se ha combinado en la base de datos o que se combinará en la base de datos. La característica debe existir antes de llamar a este método.

Un módulo de combinación nunca debe entregar un componente que contenga archivos del sistema a la característica principal de una aplicación, ya que esto puede hacer que el instalador valide y repare la aplicación cada vez que se usa el archivo del sistema. Se debe .msi un archivo de .msi que está diseñado para aceptar componentes de un módulo de combinación para que los componentes que contienen archivos del sistema solo pertenezcan a características independientes de la característica principal de la aplicación.

Si el paquete usa un módulo de combinación que contiene archivos del sistema que vinculan todos los componentes del módulo de mezcla a la característica principal de la aplicación, un intento de usar el archivo del sistema puede desencadenar que el instalador intente reparar la característica principal de la aplicación. Si no se puede reparar la característica principal, se puede producir un error en la instalación.

 

 



