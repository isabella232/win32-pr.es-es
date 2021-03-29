---
description: Los sistemas basados en Windows pueden tener varias instancias del tipo de objeto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: El tipo de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809295"
---
# <a name="the-trusteddomain-object-type"></a>El tipo de objeto TrustedDomain

Los sistemas basados en Windows pueden tener varias instancias del tipo de objeto [**TrustedDomain**](trusteddomain-object.md) . Los objetos **TrustedDomain** tienen dos campos que deben ser únicos entre todos los objetos **TrustedDomain** :

-   Nombre del [ **TrustedDomain**](trusteddomain-object.md)
-   El [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) de [**TrustedDomain**](trusteddomain-object.md).

Se rechazará el intento de crear un nuevo objeto **TrustedDomain** con un nombre o SID que ya esté en uso por otro objeto **TrustedDomain** .

 

 
