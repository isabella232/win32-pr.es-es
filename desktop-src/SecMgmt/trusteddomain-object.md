---
description: El objeto TrustedDomain almacena información sobre una relación de confianza con un dominio.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069001"
---
# <a name="trusteddomain-object"></a>Objeto TrustedDomain

El **objeto TrustedDomain** almacena información sobre una relación de confianza con un dominio. Se crea un objeto **TrustedDomain** en el sistema de confianza para identificar una cuenta dentro del dominio de confianza que se puede usar para enviar solicitudes de autenticación y realizar otras operaciones, como traducciones de nombres e identificadores de seguridad [](/windows/desktop/SecGloss/s-gly) (SID).

La información almacenada en un **objeto TrustedDomain** incluye:

-   SID del dominio de confianza. Esta información no es modificable y debe ser única entre todos los **objetos TrustedDomain.**
-   Nombre del dominio de confianza. Esta información no es modificable y debe ser única entre todos los **objetos TrustedDomain.**
-   Nombre de la cuenta del dominio de confianza que se usa para enviar solicitudes de autenticación y para realizar traducciones de nombre y SID. Este nombre no es modificable.
-   Contraseña usada para enviar solicitudes de autenticación y realizar traducciones de nombres y SID.

Para obtener más información, [vea El tipo de objeto TrustedDomain](the-trusteddomain-object-type.md).

 

 
