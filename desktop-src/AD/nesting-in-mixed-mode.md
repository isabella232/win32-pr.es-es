---
title: Anidamiento en modo mixto
description: En este tema se enumeran las restricciones de los grupos de seguridad en un dominio de modo mixto.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Anidamiento en AD en modo mixto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c53fd79cb10c452dbb363c3d6803071e6e52871f0ce87b03f9d06a61eaece8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185828"
---
# <a name="nesting-in-mixed-mode"></a>Anidamiento en modo mixto

En este tema se enumeran las restricciones de los grupos de seguridad en un dominio de modo mixto.

Los grupos de seguridad de un dominio de modo mixto tienen las siguientes restricciones:

-   Los grupos universales no se pueden crear en dominios de modo mixto porque el ámbito universal solo se admite Windows 2000 dominios en modo nativo.
-   Un grupo global puede contener cuentas del mismo dominio al que pertenece el grupo. Un grupo global no puede contener ningún grupo universal, ningún grupo global o una cuenta de otro dominio.
-   Un grupo local de dominio puede contener grupos globales y cuentas de cualquier dominio o bosque. Un grupo local de dominio no puede contener ningún otro grupo local de dominio.

Tenga en cuenta que los grupos de distribución se pueden anidar según las reglas de anidamiento para el modo nativo.

 

 




