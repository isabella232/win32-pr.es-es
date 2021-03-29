---
title: Anidar en modo nativo
description: En la lista siguiente se describe lo que puede incluirse en un grupo que existe en un dominio de modo nativo.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Anidar en AD en modo nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903101"
---
# <a name="nesting-in-native-mode"></a>Anidar en modo nativo

En la lista siguiente se describe lo que puede incluirse en un grupo que existe en un dominio de modo nativo. Esta misma lista también se aplica a los grupos de distribución en dominios de modo mixto. El ámbito del Grupo determina las reglas de contención.

-   Un grupo universal puede contener otros grupos universales, grupos globales y cuentas de cualquier dominio del bosque en el que reside este grupo universal.
-   Un grupo global puede contener otros grupos y cuentas globales del mismo dominio al que pertenece el grupo. Un grupo global no puede contener grupos universales ni cualquier grupo o cuenta global de otro dominio.
-   Un grupo local de dominio puede contener grupos universales, grupos globales y cuentas de cualquier dominio o bosque. Un grupo local de dominio también puede contener otros grupos locales de dominio del mismo dominio al que pertenece el grupo. Un grupo local de dominio no puede contener otros grupos locales de dominio de ningún otro dominio o bosque.

 

 




