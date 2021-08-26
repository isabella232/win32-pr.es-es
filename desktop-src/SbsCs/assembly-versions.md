---
description: Cada ensamblado en paralelo debe tener una versión.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versiones de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e555035bf7b43f53d3a68f249005928867f453b78522f70dd45f3b5379c75e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885575"
---
# <a name="assembly-versions"></a>Versiones de ensamblado

Cada ensamblado en paralelo debe tener una versión. Cada versión de ensamblado está asociada a un número de versión que tiene cuatro partes separadas por puntos: *major.minor.build.revision*. Si se realiza un cambio en un ensamblado  que  lo hace incompatible con las versiones existentes, se deben cambiar las partes principales o secundarias del número de versión. Un número de versión que cambia solo en los elementos *de* compilación *o* revisión indica que el ensamblado es compatible con versiones anteriores.

La versión debe especificarse en los **elementos assemblyIdentity** de [los manifiestos](manifests.md). Use el formato de versión de cuatro partes: mmmmm.nnnnn.ooooo.ppppp. Cada una de las partes separadas por puntos puede ser de 0 a 65535, ambos incluidos.

 

 



