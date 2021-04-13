---
title: CB_TARGET_INFO estructura (Cbclient. h)
description: Contiene información sobre el equipo de destino y las direcciones IP donde se deben redirigir las conexiones entrantes.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- Estructura de CB_TARGET_INFO Servicios de Escritorio remoto
- PCB_TARGET_INFO puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422089"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="68012-105">Estructura de información del \_ destino CB \_</span><span class="sxs-lookup"><span data-stu-id="68012-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="68012-106">Contiene información sobre el equipo de destino y las direcciones IP donde se deben redirigir las conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="68012-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="68012-107">Esta estructura se usa con el método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="68012-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68012-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68012-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="68012-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="68012-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="68012-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="68012-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="68012-111">Representa el nombre de dominio completo del servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="68012-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="68012-112">En un escenario de virtualización de Escritorio remoto (RDV), este miembro es **null**.</span><span class="sxs-lookup"><span data-stu-id="68012-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="68012-113">En un escenario de host de sesión Escritorio remoto (RDSH), este miembro contiene el nombre del servidor al que se redirige la conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="68012-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="68012-114">**AddressCount**</span><span class="sxs-lookup"><span data-stu-id="68012-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="68012-115">El número de entradas válidas en la matriz **Addresses** .</span><span class="sxs-lookup"><span data-stu-id="68012-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="68012-116">**Direcciones**</span><span class="sxs-lookup"><span data-stu-id="68012-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="68012-117">Matriz de cadenas que contienen las direcciones IP a las que se redirigen las conexiones entrantes.</span><span class="sxs-lookup"><span data-stu-id="68012-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="68012-118">El número de elementos válidos en esta matriz se especifica en el miembro **AddressCount** .</span><span class="sxs-lookup"><span data-stu-id="68012-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68012-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68012-119">Requirements</span></span>



| <span data-ttu-id="68012-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68012-120">Requirement</span></span> | <span data-ttu-id="68012-121">Value</span><span class="sxs-lookup"><span data-stu-id="68012-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68012-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68012-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68012-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68012-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="68012-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68012-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68012-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68012-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="68012-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68012-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68012-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="68012-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68012-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="68012-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68012-129">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="68012-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





