---
title: Cambiar el ámbito o el tipo de un grupo
description: En este tema se muestra cómo cambiar el ámbito o el tipo de un grupo en dominios de modo nativo.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- agrupar AD, cambiar el ámbito o el tipo de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772744"
---
# <a name="changing-a-groups-scope-or-type"></a>Cambiar el ámbito o el tipo de un grupo

No se permite cambiar un tipo o ámbito de grupo en dominios de modo mixto. Sin embargo, en los dominios de modo nativo se permiten las siguientes conversiones:

Grupo global a grupo universal: solo se permite si el grupo global no es miembro de otro grupo global.

Grupo local de dominio a grupo universal: el grupo local de dominio que se va a convertir no puede contener otro grupo local de dominio.

Grupo universal a grupo local de dominio o global: para la conversión al grupo global, el grupo universal que se está convirtiendo no puede contener usuarios o grupos globales de otro dominio. Para la conversión a un grupo local de dominio, el grupo universal que se va a convertir no puede ser miembro de ningún grupo universal o de un grupo local de dominio de otro dominio.

En modo nativo, un tipo de grupo se puede convertir libremente entre grupos de seguridad y grupos de distribución.

Tenga en cuenta que si se usa un grupo para establecer el control de acceso, el cambio de ámbito o tipo puede afectar a las entradas de control de acceso (ACE) que contienen ese grupo. El sistema de seguridad omitirá las ACE que contienen grupos que no son grupos de seguridad.

 

 




