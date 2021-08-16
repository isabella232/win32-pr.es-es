---
description: Windows basados en aplicaciones pueden tener varias instancias del tipo de objeto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: El tipo de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab860f9192e48433242251578a20a45bf294164c0bffff8b6f00562a1442e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004843"
---
# <a name="the-trusteddomain-object-type"></a>El tipo de objeto TrustedDomain

Windows basados en aplicaciones pueden tener varias instancias del tipo [**de objeto TrustedDomain.**](trusteddomain-object.md) **Los objetos TrustedDomain** tienen dos campos que deben ser únicos entre todos los **objetos TrustedDomain:**

-   Nombre de [ **TrustedDomain**](trusteddomain-object.md)
-   Identificador [*de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) de [**TrustedDomain.**](trusteddomain-object.md)

Se rechazará un intento de crear un nuevo objeto **TrustedDomain** con un nombre o SID que ya esté en uso por otro objeto **TrustedDomain.**

 

 
