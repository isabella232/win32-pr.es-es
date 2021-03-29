---
title: Anidar en modo mixto
description: En este tema se enumeran las restricciones de los grupos de seguridad en un dominio de modo mixto.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Anidar en AD en modo mixto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903102"
---
# <a name="nesting-in-mixed-mode"></a>Anidar en modo mixto

En este tema se enumeran las restricciones de los grupos de seguridad en un dominio de modo mixto.

Los grupos de seguridad en un dominio de modo mixto tienen las siguientes restricciones:

-   No se pueden crear grupos universales en dominios de modo mixto porque el ámbito universal solo es compatible con dominios de modo nativo de Windows 2000.
-   Un grupo global puede contener cuentas del mismo dominio al que pertenece el grupo. Un grupo global no puede contener grupos universales, ningún grupo global o una cuenta de otro dominio.
-   Un grupo local de dominio puede contener grupos y cuentas globales de cualquier dominio o bosque. Un grupo local de dominio no puede contener ningún otro grupo local de dominio.

Tenga en cuenta que los grupos de distribución se pueden anidar según las reglas de anidamiento del modo nativo.

 

 




