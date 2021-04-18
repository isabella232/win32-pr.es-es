---
description: 'La API del proveedor de espacio de nombres PNRP utiliza las siguientes estructuras:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Estructuras PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667386"
---
# <a name="pnrp-structures"></a><span data-ttu-id="9abf6-103">Estructuras PNRP</span><span class="sxs-lookup"><span data-stu-id="9abf6-103">PNRP Structures</span></span>

<span data-ttu-id="9abf6-104">La API del proveedor de espacio de nombres PNRP utiliza las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="9abf6-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="9abf6-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="9abf6-105">Structure</span></span>                                                             | <span data-ttu-id="9abf6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9abf6-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9abf6-107">**\_información del \_ punto de conexión PNRP del mismo nivel \_**</span><span class="sxs-lookup"><span data-stu-id="9abf6-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="9abf6-108">Contiene las direcciones IP y los datos asociados a un punto de conexión del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="9abf6-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="9abf6-109">**\_información de \_ la nube PNRP del mismo nivel \_**</span><span class="sxs-lookup"><span data-stu-id="9abf6-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="9abf6-110">Contiene información sobre una nube de protocolo de resolución de nombres de mismo nivel (PNRP).</span><span class="sxs-lookup"><span data-stu-id="9abf6-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="9abf6-111">**\_información de \_ registro de PNRP del mismo nivel \_**</span><span class="sxs-lookup"><span data-stu-id="9abf6-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="9abf6-112">Contiene la información proporcionada por una identidad del mismo nivel cuando se registra con una nube PNRP.</span><span class="sxs-lookup"><span data-stu-id="9abf6-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="9abf6-113">PNRP y BLOB</span><span class="sxs-lookup"><span data-stu-id="9abf6-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="9abf6-114">Pasa datos a la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante las llamadas a varias funciones.</span><span class="sxs-lookup"><span data-stu-id="9abf6-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="9abf6-115">PNRP y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="9abf6-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="9abf6-116">Facilita la resolución de nombres y la enumeración de nombres y nubes.</span><span class="sxs-lookup"><span data-stu-id="9abf6-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="9abf6-117">**\_identificador de nube PNRP \_**</span><span class="sxs-lookup"><span data-stu-id="9abf6-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="9abf6-118">Contiene los valores que definen una nube de red.</span><span class="sxs-lookup"><span data-stu-id="9abf6-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="9abf6-119">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="9abf6-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="9abf6-120">Apuntado por el miembro **lpBlob** de la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="9abf6-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="9abf6-121">**PNRPINFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="9abf6-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="9abf6-122">Apuntado por el miembro **lpBlob** de la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="9abf6-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="9abf6-123">[**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9abf6-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="9abf6-124">Apuntado por el miembro **lpBlob** de la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) y proporciona compatibilidad con datos opacos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9abf6-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
