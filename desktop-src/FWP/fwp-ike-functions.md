---
title: Funciones de IKE/AuthIP
description: Funciones de (WFP) utilizadas para interactuar con los módulos de creación de claves \ 8212; Intercambio de claves por red (IKE), Intercambio de claves por red V2 (IKEv2) y protocolo de Internet autenticado (AuthIP).
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- Funciones de Intercambio de claves por red de la API de la plataforma de filtrado de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357360"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="76847-104">Funciones de IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="76847-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="76847-105">Las funciones de la plataforma de filtrado de Windows (WFP) utilizadas para interactuar con los módulos de creación de claves (Intercambio de claves por red (IKE), Intercambio de claves por red V2 (IKEv2) y protocolo de Internet autenticado (AuthIP), son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="76847-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="76847-106">IkeextGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="76847-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="76847-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="76847-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="76847-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="76847-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="76847-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="76847-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="76847-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="76847-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="76847-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="76847-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="76847-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="76847-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="76847-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="76847-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="76847-114">IkeextSaEnum:</span><span class="sxs-lookup"><span data-stu-id="76847-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="76847-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="76847-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="76847-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="76847-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="76847-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="76847-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="76847-118">IkeextSaGetById:</span><span class="sxs-lookup"><span data-stu-id="76847-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="76847-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="76847-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="76847-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="76847-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="76847-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="76847-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 




