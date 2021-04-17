---
description: Los nombres del mismo nivel se usan en el protocolo de resolución de nombres de mismo nivel (PNRP), el administrador de identidad del mismo nivel y la infraestructura de agrupación del mismo nivel.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Nombres de mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667399"
---
# <a name="peer-names"></a><span data-ttu-id="ecbca-103">Nombres de mismo nivel</span><span class="sxs-lookup"><span data-stu-id="ecbca-103">Peer Names</span></span>

<span data-ttu-id="ecbca-104">Los nombres del mismo nivel se usan en el protocolo de resolución de nombres de mismo nivel (PNRP), el administrador de identidad del mismo nivel y la infraestructura de agrupación del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ecbca-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="ecbca-105">Los nombres de mismo nivel son nombres estables para recursos como equipos, usuarios, grupos o servicios.</span><span class="sxs-lookup"><span data-stu-id="ecbca-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="ecbca-106">PNRP usa nombres de mismo nivel para identificar nodos en una red del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ecbca-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="ecbca-107">Un punto de conexión que usa la infraestructura del mismo nivel es realmente una tupla que consta de una dirección IPv4 o IPv6, un puerto y un protocolo (TCP o UDP).</span><span class="sxs-lookup"><span data-stu-id="ecbca-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="ecbca-108">Un nombre del mismo nivel puede tener más de una tupla.</span><span class="sxs-lookup"><span data-stu-id="ecbca-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="ecbca-109">Un nombre del mismo nivel es una cadena de texto que tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="ecbca-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="ecbca-110">"Autoridad. clasificador"</span><span class="sxs-lookup"><span data-stu-id="ecbca-110">"Authority.Classifier"</span></span>

<span data-ttu-id="ecbca-111">El valor de una autoridad depende de si el nombre es seguro o no seguro.</span><span class="sxs-lookup"><span data-stu-id="ecbca-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="ecbca-112">El clasificador de un nombre del mismo nivel es una cadena.</span><span class="sxs-lookup"><span data-stu-id="ecbca-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="ecbca-113">Un clasificador puede ser cualquier nombre que contenga 150 o menos caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ecbca-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="ecbca-114">Los nombres del mismo nivel distinguen mayúsculas de minúsculas y se pueden registrar como protegidos o no seguros.</span><span class="sxs-lookup"><span data-stu-id="ecbca-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="ecbca-115">En la lista siguiente se identifican algunos ejemplos de nombres de mismo nivel:</span><span class="sxs-lookup"><span data-stu-id="ecbca-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="ecbca-116">"0. MyUnsecuredPeerName"</span><span class="sxs-lookup"><span data-stu-id="ecbca-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="ecbca-117">"0. \ \ \ \ \ \ \ \. Games"</span><span class="sxs-lookup"><span data-stu-id="ecbca-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="ecbca-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d. Johndoe</span><span class="sxs-lookup"><span data-stu-id="ecbca-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="ecbca-119">Nombres de mismo nivel seguros</span><span class="sxs-lookup"><span data-stu-id="ecbca-119">Secure Peer Names</span></span>

<span data-ttu-id="ecbca-120">Para un nombre seguro, la autoridad es el hash del algoritmo hash seguro (SHA) de la clave pública del nombre del mismo nivel y da como resultado una cadena hexadecimal de 40 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ecbca-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="ecbca-121">Un nombre seguro de mismo nivel solo se puede registrar con PNRP mediante el propietario o el delegado del propietario del nombre del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ecbca-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="ecbca-122">Se debe crear un nombre de mismo nivel protegido mediante una llamada a [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span><span class="sxs-lookup"><span data-stu-id="ecbca-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="ecbca-123">Nombres de mismo nivel no seguros</span><span class="sxs-lookup"><span data-stu-id="ecbca-123">Unsecured Peer Names</span></span>

<span data-ttu-id="ecbca-124">Para un nombre no seguro, la autoridad es cero (0) y el clasificador es la única parte significativa del nombre del mismo nivel, que crea un nombre del mismo nivel no seguro sin una [identidad](identity-manager-api.md)asociada.</span><span class="sxs-lookup"><span data-stu-id="ecbca-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="ecbca-125">Los nombres de mismo nivel no seguros se usan en el registro y la resolución de nombres PNRP.</span><span class="sxs-lookup"><span data-stu-id="ecbca-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="ecbca-126">Los nombres de mismo nivel no seguros proporcionan una manera útil de registrar y resolver recursos que no requieren una resolución de nombres segura.</span><span class="sxs-lookup"><span data-stu-id="ecbca-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="ecbca-127">Sin embargo, cualquier nodo puede publicar cualquier nombre no seguro.</span><span class="sxs-lookup"><span data-stu-id="ecbca-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="ecbca-128">Las aplicaciones preocupadas por la seguridad deben asegurarse de que son sólidas y seguras en su consumo de nombres del mismo nivel no seguros.</span><span class="sxs-lookup"><span data-stu-id="ecbca-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="ecbca-129">Cualquier usuario puede registrar un nombre de mismo nivel no seguro con PNRP.</span><span class="sxs-lookup"><span data-stu-id="ecbca-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="ecbca-130">PNRP y la instancia de nombre del mismo nivel más cercana</span><span class="sxs-lookup"><span data-stu-id="ecbca-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="ecbca-131">Puede haber más de una instancia de un nombre de mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ecbca-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="ecbca-132">Cuando se usa [PNRP](pnrp-namespace-provider-api.md) para resolver un nombre del mismo nivel, hay un concepto de una instancia de nombre del mismo nivel **más cercana** , lo que significa que el nombre tiene una ubicación de servicio más cercana al miembro **saHint** especificado en [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) o [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ecbca-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="ecbca-133">Si no se proporciona ninguna sugerencia, más cercana a una de las direcciones IP locales.</span><span class="sxs-lookup"><span data-stu-id="ecbca-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 
