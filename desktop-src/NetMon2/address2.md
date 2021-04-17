---
description: Contiene una dirección única de cualquier tipo de direcciones admitidas.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: DIRECCIÓN2 (estructura) (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667127"
---
# <a name="address2-structure"></a><span data-ttu-id="88537-103">DIRECCIÓN2 (estructura)</span><span class="sxs-lookup"><span data-stu-id="88537-103">ADDRESS2 structure</span></span>

<span data-ttu-id="88537-104">La estructura de la **Dirección** contiene una dirección única de cualquier tipo de direcciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="88537-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="88537-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88537-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="88537-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="88537-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88537-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="88537-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="88537-108">Tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="88537-108">Address type.</span></span> <span data-ttu-id="88537-109">Los valores pueden ser cualquier de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="88537-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="88537-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="88537-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="88537-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="88537-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="88537-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="88537-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="88537-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="88537-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="88537-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="88537-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="88537-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="88537-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="88537-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="88537-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="88537-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="88537-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="88537-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="88537-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="88537-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="88537-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="88537-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="88537-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="88537-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="88537-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="88537-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="88537-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="88537-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="88537-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="88537-124">**Mac**</span><span class="sxs-lookup"><span data-stu-id="88537-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-125">Vista de los datos expresada como una dirección MAC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="88537-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-126">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-127">Vista de los datos expresada como una dirección IP sin procesar.</span><span class="sxs-lookup"><span data-stu-id="88537-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="88537-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="88537-129">Vista de los datos expresada como una dirección IP versión 6 sin procesar.</span><span class="sxs-lookup"><span data-stu-id="88537-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-130">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-131">Vista de los datos expresada como una dirección IPX sin procesar.</span><span class="sxs-lookup"><span data-stu-id="88537-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-132">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-133">Vista de los datos expresada como un valor de dirección IPX descodificada.</span><span class="sxs-lookup"><span data-stu-id="88537-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="88537-134">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-135">Vista de los datos expresada como una dirección IP de Vines sin procesar.</span><span class="sxs-lookup"><span data-stu-id="88537-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-136">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-137">Vista de los datos expresada como una dirección IP de Vines descodificada.</span><span class="sxs-lookup"><span data-stu-id="88537-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-138">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-139">Vista de los datos expresada como una dirección de origen Ethernet.</span><span class="sxs-lookup"><span data-stu-id="88537-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-140">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-141">Vista de los datos expresada como una dirección de destino Ethernet.</span><span class="sxs-lookup"><span data-stu-id="88537-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-142">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-143">Una vista de los datos como una dirección de origen de token ring.</span><span class="sxs-lookup"><span data-stu-id="88537-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-144">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-145">Una vista de los datos como una dirección de destino de token ring.</span><span class="sxs-lookup"><span data-stu-id="88537-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-146">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-147">Vista de los datos expresada como una dirección de origen FDDI.</span><span class="sxs-lookup"><span data-stu-id="88537-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-148">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="88537-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88537-149">Vista de los datos expresada como una dirección de destino FDDI.</span><span class="sxs-lookup"><span data-stu-id="88537-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="88537-150">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="88537-150">**Flags**</span></span>
<span data-ttu-id="88537-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="88537-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="88537-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88537-152">Requirements</span></span>



| <span data-ttu-id="88537-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="88537-153">Requirement</span></span> | <span data-ttu-id="88537-154">Value</span><span class="sxs-lookup"><span data-stu-id="88537-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88537-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88537-155">Minimum supported client</span></span><br/> | <span data-ttu-id="88537-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="88537-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="88537-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88537-157">Minimum supported server</span></span><br/> | <span data-ttu-id="88537-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88537-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88537-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88537-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="88537-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="88537-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




