---
description: El objeto TrustedDomain almacena información acerca de una relación de confianza con un dominio.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907814"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="92337-103">Objeto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="92337-103">TrustedDomain Object</span></span>

<span data-ttu-id="92337-104">El objeto **TrustedDomain** almacena información acerca de una relación de confianza con un dominio.</span><span class="sxs-lookup"><span data-stu-id="92337-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="92337-105">Un objeto **TrustedDomain** se crea en el sistema de confianza para identificar una cuenta en el dominio de confianza que se puede usar para enviar solicitudes de autenticación y para realizar otras operaciones, como traducciones de nombre y de [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID).</span><span class="sxs-lookup"><span data-stu-id="92337-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="92337-106">La información almacenada en un objeto **TrustedDomain** incluye:</span><span class="sxs-lookup"><span data-stu-id="92337-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="92337-107">SID del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="92337-107">The SID of the trusted domain.</span></span> <span data-ttu-id="92337-108">Esta información no es modificable y debe ser única entre todos los objetos **TrustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="92337-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="92337-109">Nombre del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="92337-109">The name of the trusted domain.</span></span> <span data-ttu-id="92337-110">Esta información no es modificable y debe ser única entre todos los objetos **TrustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="92337-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="92337-111">El nombre de la cuenta en el dominio de confianza que se usa para enviar solicitudes de autenticación y para realizar traducciones de nombres y SID.</span><span class="sxs-lookup"><span data-stu-id="92337-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="92337-112">Este nombre no es modificable.</span><span class="sxs-lookup"><span data-stu-id="92337-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="92337-113">Contraseña usada para enviar solicitudes de autenticación y realizar traducciones de nombres y SID.</span><span class="sxs-lookup"><span data-stu-id="92337-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="92337-114">Para obtener más información, vea [el tipo de objeto TrustedDomain](the-trusteddomain-object-type.md).</span><span class="sxs-lookup"><span data-stu-id="92337-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 
