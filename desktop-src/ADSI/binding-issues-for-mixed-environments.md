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
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="6c483-104">Problemas de enlace para entornos mixtos</span><span class="sxs-lookup"><span data-stu-id="6c483-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="6c483-105">En entornos en los que el dominio que contiene Active Directory tiene una relación de confianza con un dominio de Windows NT 4,0, puede haber un problema con el uso de enlaces sin servidor para enlazar a objetos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6c483-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="6c483-106">En algunos entornos de red, se han configurado relaciones de confianza entre los controladores de dominio que contienen Active Directory y los servidores Windows NT 4,0 con el fin de permitir la autenticación entre dominios.</span><span class="sxs-lookup"><span data-stu-id="6c483-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="6c483-107">En estos entornos mixtos, si un usuario, que es miembro de Windows NT 4,0, intenta usar el enlace sin servidor para enlazar a un objeto de Active Directory en un dominio de confianza, se producirá un error en el enlace y se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="6c483-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="6c483-108">Esto se debe a que un enlace sin servidor utiliza la función [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) para enlazar con el objeto en Active Directory, que depende del DNS adecuado.</span><span class="sxs-lookup"><span data-stu-id="6c483-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="6c483-109">En este escenario, el usuario de Windows NT debe proporcionar el nombre de un dominio específico con el que enlazar.</span><span class="sxs-lookup"><span data-stu-id="6c483-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="6c483-110">A continuación se muestra un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6c483-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 