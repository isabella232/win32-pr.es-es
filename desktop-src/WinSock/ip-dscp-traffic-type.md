---
description: En la tabla siguiente se \_ describen \_ las opciones de socket de tipo de tráfico de DSCP IP \_ .
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653649"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="b6ab4-103">\_tipo de \_ tráfico IP DSCP \_</span><span class="sxs-lookup"><span data-stu-id="b6ab4-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="b6ab4-104">En la tabla siguiente se \_ describen \_ las opciones de socket de tipo de tráfico de DSCP IP \_ .</span><span class="sxs-lookup"><span data-stu-id="b6ab4-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="b6ab4-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_tipo de \_ tráfico IP DSCP \_**</dt> </span><span class="sxs-lookup"><span data-stu-id="b6ab4-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="b6ab4-106">Opción</span><span class="sxs-lookup"><span data-stu-id="b6ab4-106">Option</span></span>              | <span data-ttu-id="b6ab4-107">Obtener</span><span class="sxs-lookup"><span data-stu-id="b6ab4-107">Get</span></span> | <span data-ttu-id="b6ab4-108">Set</span><span class="sxs-lookup"><span data-stu-id="b6ab4-108">Set</span></span> | <span data-ttu-id="b6ab4-109">Tipo Optval</span><span class="sxs-lookup"><span data-stu-id="b6ab4-109">Optval Type</span></span> | <span data-ttu-id="b6ab4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6ab4-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ab4-111">\_tipo de tráfico de DSCP \_</span><span class="sxs-lookup"><span data-stu-id="b6ab4-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="b6ab4-112">Sí</span><span class="sxs-lookup"><span data-stu-id="b6ab4-112">Yes</span></span> | <span data-ttu-id="b6ab4-113">Sí</span><span class="sxs-lookup"><span data-stu-id="b6ab4-113">Yes</span></span> | <span data-ttu-id="b6ab4-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="b6ab4-114">DWORD</span></span>       | <span data-ttu-id="b6ab4-115">Al establecer este valor en los valores definidos en el **\_ \_ tipo de tráfico de DSCP**, una aplicación podrá solicitar que los paquetes de red se traten según el tipo de servicio que se solicita.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="b6ab4-116">De forma similar, se pueden utilizar llamadas a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obtener la configuración actual del tipo de tráfico solicitado en el socket dado.</span><span class="sxs-lookup"><span data-stu-id="b6ab4-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6ab4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6ab4-117">Requirements</span></span>



| <span data-ttu-id="b6ab4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ab4-118">Requirement</span></span> | <span data-ttu-id="b6ab4-119">Value</span><span class="sxs-lookup"><span data-stu-id="b6ab4-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b6ab4-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b6ab4-120">End of client support</span></span><br/> | <span data-ttu-id="b6ab4-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6ab4-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="b6ab4-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b6ab4-122">End of server support</span></span><br/> | <span data-ttu-id="b6ab4-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b6ab4-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="b6ab4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6ab4-124">Header</span></span><br/>                | <dl> <span data-ttu-id="b6ab4-125"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab4-125"><dt>N/A</dt></span></span> </dl> |



 

 




