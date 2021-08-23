---
title: Anidamiento en modo nativo
description: En la lista siguiente se describe lo que puede incluirse en un grupo que existe en un dominio en modo nativo.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Anidamiento en AD en modo nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3fa2842981354738cd4ef112ef278fa33ca310adeedcd62fb245a2663cce07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025743"
---
# <a name="nesting-in-native-mode"></a>Anidamiento en modo nativo

En la lista siguiente se describe lo que puede incluirse en un grupo que existe en un dominio en modo nativo. Esta misma lista también se aplica a los grupos de distribución en dominios de modo mixto. El ámbito del grupo determina estas reglas de contención.

-   Un grupo universal puede contener otros grupos universales, grupos globales y cuentas de cualquier dominio dentro del bosque en el que reside este grupo universal.
-   Un grupo global puede contener otros grupos globales y cuentas del mismo dominio al que pertenece el grupo. Un grupo global no puede contener ningún grupo universal ni ningún grupo global o cuenta de otro dominio.
-   Un grupo local de dominio puede contener grupos universales, grupos globales y cuentas de cualquier dominio o bosque. Un grupo local de dominio también puede contener otros grupos locales de dominio del mismo dominio al que pertenece el grupo. Un grupo local de dominio no puede contener otros grupos locales de dominio de ningún otro dominio o bosque.

 

 




