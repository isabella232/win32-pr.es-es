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
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="082e9-104">Detección del modo de operación de un dominio</span><span class="sxs-lookup"><span data-stu-id="082e9-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="082e9-105">En Windows 2000, un dominio puede ejecutarse en dos modos de operación: mixto y nativo.</span><span class="sxs-lookup"><span data-stu-id="082e9-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="082e9-106">El modo mixto debe usarse para incluir controladores de dominio que ejecuten Windows NT 4,0 en un dominio de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="082e9-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="082e9-107">El modo mixto no admite grupos universales o grupos anidados.</span><span class="sxs-lookup"><span data-stu-id="082e9-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="082e9-108">Si todos los controladores de dominio del dominio ejecutan Windows 2000, puede usar el modo nativo.</span><span class="sxs-lookup"><span data-stu-id="082e9-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="082e9-109">Para detectar mediante programación el modo de operación de un dominio de Windows 2000, lea la propiedad [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) del objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) para ese dominio.</span><span class="sxs-lookup"><span data-stu-id="082e9-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="082e9-110">Un valor de cero (0) significa que el dominio está en modo nativo.</span><span class="sxs-lookup"><span data-stu-id="082e9-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="082e9-111">Un valor de uno (1) indica que el dominio está en modo mixto.</span><span class="sxs-lookup"><span data-stu-id="082e9-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="082e9-112">También puede usar la función [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) para obtener el modo de operación, así como otros datos sobre el dominio y su estado.</span><span class="sxs-lookup"><span data-stu-id="082e9-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="082e9-113">Para enlazar con el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) del dominio de la cuenta de usuario en la que se ejecuta la aplicación, use el enlace sin servidor y RootDSE para obtener el nombre distintivo del dominio y, a continuación, use ese nombre distintivo para enlazar con el objeto **domainDNS** que representa ese dominio.</span><span class="sxs-lookup"><span data-stu-id="082e9-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="082e9-114">Para obtener más información sobre el enlace sin servidor y rootDSE, vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="082e9-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="082e9-115">Para obtener más información y un ejemplo de código que muestra cómo detectar mediante programación el modo de operación de un dominio, vea [el código de ejemplo para determinar el modo de operación](example-code-for-determining-the-operation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="082e9-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 