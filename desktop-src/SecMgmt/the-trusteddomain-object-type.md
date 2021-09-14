---
description: Windows basados en aplicaciones pueden tener varias instancias del tipo de objeto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: El tipo de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069004"
---
# <a name="the-trusteddomain-object-type"></a>El tipo de objeto TrustedDomain

Windows basados en aplicaciones pueden tener varias instancias del tipo de objeto [**TrustedDomain.**](trusteddomain-object.md) **Los objetos TrustedDomain** tienen dos campos que deben ser únicos entre todos los **objetos TrustedDomain:**

-   Nombre de [ **TrustedDomain**](trusteddomain-object.md)
-   Identificador [*de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) de [**TrustedDomain.**](trusteddomain-object.md)

Se rechazará un intento de crear un nuevo objeto **TrustedDomain** con un nombre o SID que ya esté en uso por otro objeto **TrustedDomain.**

 

 
