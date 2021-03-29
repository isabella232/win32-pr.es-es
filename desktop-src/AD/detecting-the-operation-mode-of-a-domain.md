---
title: Detección del modo de operación de un dominio
description: En Windows 2000, un dominio puede ejecutarse en dos modos de operación mixto y nativo.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Detección del modo de operación de un dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904506"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a>Detección del modo de operación de un dominio

En Windows 2000, un dominio puede ejecutarse en dos modos de operación: mixto y nativo. El modo mixto debe usarse para incluir controladores de dominio que ejecuten Windows NT 4,0 en un dominio de Windows 2000. El modo mixto no admite grupos universales o grupos anidados. Si todos los controladores de dominio del dominio ejecutan Windows 2000, puede usar el modo nativo.

Para detectar mediante programación el modo de operación de un dominio de Windows 2000, lea la propiedad [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) del objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) para ese dominio. Un valor de cero (0) significa que el dominio está en modo nativo. Un valor de uno (1) indica que el dominio está en modo mixto. También puede usar la función [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) para obtener el modo de operación, así como otros datos sobre el dominio y su estado.

Para enlazar con el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) del dominio de la cuenta de usuario en la que se ejecuta la aplicación, use el enlace sin servidor y RootDSE para obtener el nombre distintivo del dominio y, a continuación, use ese nombre distintivo para enlazar con el objeto **domainDNS** que representa ese dominio. Para obtener más información sobre el enlace sin servidor y rootDSE, vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).

Para obtener más información y un ejemplo de código que muestra cómo detectar mediante programación el modo de operación de un dominio, vea [el código de ejemplo para determinar el modo de operación](example-code-for-determining-the-operation-mode.md).

 

 