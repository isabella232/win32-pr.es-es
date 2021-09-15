---
description: Cada ensamblado en paralelo debe tener una versión.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versiones de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271719"
---
# <a name="assembly-versions"></a>Versiones de ensamblado

Cada ensamblado en paralelo debe tener una versión. Cada versión del ensamblado está asociada a un número de versión que tiene cuatro partes separadas por puntos: *major.minor.build.revision*. Si se realiza un cambio en un ensamblado  que  lo hace incompatible con las versiones existentes, se deben cambiar las partes principales o secundarias del número de versión. Un número de versión que cambia solo en los elementos *de* compilación *o* revisión indica que el ensamblado es compatible con versiones anteriores.

La versión debe especificarse en los **elementos assemblyIdentity** de [los manifiestos](manifests.md). Use el formato de versión de cuatro partes: mmmmm.nnnnn.ooooo.ppppp. Cada una de las partes separadas por puntos puede ser de 0 a 65535, ambos incluidos.

 

 



