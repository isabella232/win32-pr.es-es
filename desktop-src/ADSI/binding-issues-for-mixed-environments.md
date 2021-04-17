---
title: Problemas de enlace para entornos mixtos
description: Problemas de enlace para entornos mixtos
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, problemas de enlace para entornos mixtos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656393"
---
# <a name="binding-issues-for-mixed-environments"></a>Problemas de enlace para entornos mixtos

En entornos en los que el dominio que contiene Active Directory tiene una relación de confianza con un dominio de Windows NT 4,0, puede haber un problema con el uso de enlaces sin servidor para enlazar a objetos de Active Directory.

En algunos entornos de red, se han configurado relaciones de confianza entre los controladores de dominio que contienen Active Directory y los servidores Windows NT 4,0 con el fin de permitir la autenticación entre dominios. En estos entornos mixtos, si un usuario, que es miembro de Windows NT 4,0, intenta usar el enlace sin servidor para enlazar a un objeto de Active Directory en un dominio de confianza, se producirá un error en el enlace y se devolverá un error. Esto se debe a que un enlace sin servidor utiliza la función [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) para enlazar con el objeto en Active Directory, que depende del DNS adecuado.

En este escenario, el usuario de Windows NT debe proporcionar el nombre de un dominio específico con el que enlazar. A continuación se muestra un ejemplo.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 