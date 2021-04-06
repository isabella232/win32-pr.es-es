---
title: RAS_PPP_PROJECTION_RESULT estructura (rassapi. h)
description: La \_ estructura del \_ resultado de la proyección PPP \_ de Ras se utiliza para notificar los resultados de las distintas operaciones de proyección de PPP para un puerto.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT de la estructura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802497"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="d1078-104">Estructura del resultado de la \_ proyección PPP de Ras \_ \_</span><span class="sxs-lookup"><span data-stu-id="d1078-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="d1078-105">\[La estructura del resultado de la **\_ \_ proyección \_ PPP de Ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="d1078-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="d1078-106">La estructura del resultado de la **\_ \_ proyección \_ PPP de Ras** se utiliza para notificar los resultados de las distintas operaciones de proyección de PPP para un puerto.</span><span class="sxs-lookup"><span data-stu-id="d1078-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1078-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1078-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="d1078-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1078-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1078-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="d1078-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="d1078-110">Una estructura de [**\_ \_ \_ resultado PPP NBFCP de Ras**](ras-ppp-nbfcp-result-str.md) que informa del resultado de una operación de proyección de PPP NetBEUI Framer (NBF).</span><span class="sxs-lookup"><span data-stu-id="d1078-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1078-111">**intelectual**</span><span class="sxs-lookup"><span data-stu-id="d1078-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="d1078-112">Una estructura de [**\_ \_ \_ resultados de PPP de PPP de Ras**](ras-ppp-ipcp-result-str.md) que informa del resultado de una operación de proyección del Protocolo de Internet (IP) de PPP.</span><span class="sxs-lookup"><span data-stu-id="d1078-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1078-113">**requerir**</span><span class="sxs-lookup"><span data-stu-id="d1078-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="d1078-114">Una estructura de [**\_ \_ \_ resultado de IPXCP PPP de Ras**](ras-ppp-ipxcp-result-str.md) que informa del resultado de una operación de proyección de intercambio de paquetes en la red (IPX) de PPP.</span><span class="sxs-lookup"><span data-stu-id="d1078-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1078-115">**at**</span><span class="sxs-lookup"><span data-stu-id="d1078-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="d1078-116">Una estructura de [**\_ \_ \_ resultado PPP ATCP de Ras**](ras-ppp-atcp-result-str.md) .</span><span class="sxs-lookup"><span data-stu-id="d1078-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1078-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1078-117">Remarks</span></span>

<span data-ttu-id="d1078-118">Esta estructura notifica los resultados de proyección para los protocolos NetBEUI, TCP/IP y IPX.</span><span class="sxs-lookup"><span data-stu-id="d1078-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="d1078-119">Cada estructura PPP tiene un miembro **dwError** que indica si la otra información de la estructura es válida.</span><span class="sxs-lookup"><span data-stu-id="d1078-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="d1078-120">Si **dwError** NO es un \_ error, la otra información es válida.</span><span class="sxs-lookup"><span data-stu-id="d1078-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="d1078-121">Si **dwError** es uno de los códigos de error de Winerror. h o Raserror. h, la otra información no es válida.</span><span class="sxs-lookup"><span data-stu-id="d1078-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1078-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1078-122">Requirements</span></span>



| <span data-ttu-id="d1078-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1078-123">Requirement</span></span> | <span data-ttu-id="d1078-124">Value</span><span class="sxs-lookup"><span data-stu-id="d1078-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1078-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1078-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d1078-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d1078-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d1078-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1078-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d1078-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1078-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d1078-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d1078-129">End of client support</span></span><br/>    | <span data-ttu-id="d1078-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1078-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="d1078-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d1078-131">End of server support</span></span><br/>    | <span data-ttu-id="d1078-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1078-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="d1078-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1078-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1078-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1078-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1078-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1078-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1078-136">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="d1078-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d1078-137">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d1078-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="d1078-138">**\_Puerto ras \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d1078-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="d1078-139">**\_resultado de PPP \_ ATCP \_ de Ras**</span><span class="sxs-lookup"><span data-stu-id="d1078-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="d1078-140">**resultado de PPP de PPP de RAS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d1078-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="d1078-141">**\_resultado de \_ IPXCP de PPP de Ras \_**</span><span class="sxs-lookup"><span data-stu-id="d1078-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="d1078-142">**\_resultado de \_ NBFCP de PPP de Ras \_**</span><span class="sxs-lookup"><span data-stu-id="d1078-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="d1078-143">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d1078-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





