---
title: DACL NULL y listas DACL vacías (AD DS)
description: La presencia de una lista de control de acceso discrecional (DACL) nula en el atributo nTSecurityDescriptor de cualquier objeto puede crear un riesgo de seguridad grave.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACL NULL y listas DACL vacías
- DACL AD, NULL y Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995068"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACL NULL y listas DACL vacías (AD DS)

La presencia de una lista de control de acceso discrecional (DACL) nula en el atributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de cualquier objeto puede crear un riesgo de seguridad grave. Una DACL null concede acceso completo a cualquier usuario que lo solicite; la comprobación de seguridad normal no se realiza con respecto al objeto. Una DACL null no se debería confundir con una DACL vacía. Una DACL vacía es una DACL que se ha asignado y se ha inicializado correctamente y que no contiene entradas de control de acceso (ACE). Una DACL vacía no concede ningún acceso al objeto al que se asigna.

Para obtener más información, vea [listas DACL nulas y listas DACL vacías](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 