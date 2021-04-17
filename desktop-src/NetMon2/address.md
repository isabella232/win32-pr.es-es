---
description: Está obsoleto y no debe usarse.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Estructura de dirección (Netmon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667550"
---
# <a name="address-structure"></a><span data-ttu-id="af3ca-103">Estructura de dirección</span><span class="sxs-lookup"><span data-stu-id="af3ca-103">ADDRESS structure</span></span>

<span data-ttu-id="af3ca-104">La estructura de la **Dirección** está obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="af3ca-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="af3ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af3ca-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="af3ca-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="af3ca-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="af3ca-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="af3ca-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-108">Tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="af3ca-108">Address type.</span></span> <span data-ttu-id="af3ca-109">Los valores pueden ser cualquier de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="af3ca-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="af3ca-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="af3ca-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="af3ca-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="af3ca-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="af3ca-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="af3ca-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="af3ca-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="af3ca-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="af3ca-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="af3ca-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="af3ca-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="af3ca-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="af3ca-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="af3ca-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="af3ca-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="af3ca-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="af3ca-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="af3ca-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="af3ca-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="af3ca-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="af3ca-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="af3ca-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="af3ca-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="af3ca-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="af3ca-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="af3ca-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="af3ca-123">**Mac**</span><span class="sxs-lookup"><span data-stu-id="af3ca-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-124">Vista de los datos expresada como una dirección MAC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="af3ca-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-125">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-126">Vista de los datos expresada como una dirección IP sin procesar.</span><span class="sxs-lookup"><span data-stu-id="af3ca-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-127">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-128">Vista de los datos expresada como una dirección IPX sin procesar.</span><span class="sxs-lookup"><span data-stu-id="af3ca-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-129">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-130">Vista de los datos expresada como un valor de dirección IPX descodificada.</span><span class="sxs-lookup"><span data-stu-id="af3ca-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-131">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-132">Vista de los datos expresada como una dirección IP de Vines sin procesar.</span><span class="sxs-lookup"><span data-stu-id="af3ca-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-133">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-134">Vista de los datos expresada como una dirección IP de Vines descodificada.</span><span class="sxs-lookup"><span data-stu-id="af3ca-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-135">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-136">Vista de los datos expresada como una dirección de origen Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af3ca-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-137">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-138">Vista de los datos expresada como una dirección de destino Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af3ca-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-139">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-140">Una vista de los datos como una dirección de origen de token ring.</span><span class="sxs-lookup"><span data-stu-id="af3ca-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-141">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-142">Una vista de los datos como una dirección de destino de token ring.</span><span class="sxs-lookup"><span data-stu-id="af3ca-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-143">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-144">Vista de los datos expresada como una dirección de origen FDDI.</span><span class="sxs-lookup"><span data-stu-id="af3ca-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-145">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="af3ca-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-146">Vista de los datos expresada como una dirección de destino FDDI.</span><span class="sxs-lookup"><span data-stu-id="af3ca-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="af3ca-147">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="af3ca-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="af3ca-148">Un conjunto de marcas que modifican las propiedades de dirección.</span><span class="sxs-lookup"><span data-stu-id="af3ca-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af3ca-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af3ca-149">Requirements</span></span>



| <span data-ttu-id="af3ca-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="af3ca-150">Requirement</span></span> | <span data-ttu-id="af3ca-151">Value</span><span class="sxs-lookup"><span data-stu-id="af3ca-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af3ca-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af3ca-152">Minimum supported client</span></span><br/> | <span data-ttu-id="af3ca-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="af3ca-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="af3ca-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af3ca-154">Minimum supported server</span></span><br/> | <span data-ttu-id="af3ca-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af3ca-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af3ca-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af3ca-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="af3ca-157"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="af3ca-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




