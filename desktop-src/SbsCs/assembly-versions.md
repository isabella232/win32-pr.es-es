---
description: Cada ensamblado simultáneo debe tener una versión.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versiones de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814779"
---
# <a name="assembly-versions"></a>Versiones de ensamblado

Cada ensamblado simultáneo debe tener una versión. Cada versión del ensamblado está asociada a un número de versión que tiene cuatro partes separadas por puntos: *principal. secundaria. compilación. revisión*. Si se realiza un cambio en un ensamblado que hace que sea incompatible con las versiones existentes, se deben cambiar las partes *principales* o *secundarias* del número de versión. Un número de versión que solo cambia en las partes de la *compilación* o de la *revisión* indica que el ensamblado es compatible con versiones anteriores.

La versión debe especificarse en los elementos **assemblyIdentity** de los [manifiestos](manifests.md). Use el formato de versión de cuatro partes: mmmmm. nnnnn. ooooo. ppppp. Cada una de las partes separadas por puntos puede ser 0-65535, ambos inclusive.

 

 



