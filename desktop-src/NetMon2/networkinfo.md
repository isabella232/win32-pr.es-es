---
description: La estructura NETWORKINFO describe una NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Estructura NETWORKINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818531"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="57350-103">Estructura NETWORKINFO</span><span class="sxs-lookup"><span data-stu-id="57350-103">NETWORKINFO structure</span></span>

<span data-ttu-id="57350-104">La estructura NETWORKINFO describe una NIC.</span><span class="sxs-lookup"><span data-stu-id="57350-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="57350-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57350-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="57350-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="57350-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="57350-107">**PermanentAddr**</span><span class="sxs-lookup"><span data-stu-id="57350-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="57350-108">Dirección MAC permanente.</span><span class="sxs-lookup"><span data-stu-id="57350-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="57350-109">**CurrentAddr**</span><span class="sxs-lookup"><span data-stu-id="57350-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="57350-110">Dirección MAC actual.</span><span class="sxs-lookup"><span data-stu-id="57350-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="57350-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="57350-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="57350-112">Otra dirección que admite este (por ejemplo, IP, IPX).</span><span class="sxs-lookup"><span data-stu-id="57350-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="57350-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="57350-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="57350-114">Velocidad de vínculo, en Mbps.</span><span class="sxs-lookup"><span data-stu-id="57350-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="57350-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="57350-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="57350-116">Tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="57350-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="57350-117">**MaxFrameSize**</span><span class="sxs-lookup"><span data-stu-id="57350-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="57350-118">Tamaño máximo de trama permitido.</span><span class="sxs-lookup"><span data-stu-id="57350-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="57350-119">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="57350-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="57350-120">Este parámetro puede ser una de las siguientes marcas informativas:</span><span class="sxs-lookup"><span data-stu-id="57350-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="57350-121">Value</span><span class="sxs-lookup"><span data-stu-id="57350-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="57350-122">Significado</span><span class="sxs-lookup"><span data-stu-id="57350-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="57350-123"><dt>**\_no se \_ \_ \_ admiten marcas NETWORKINFO PMODE**</dt></span><span class="sxs-lookup"><span data-stu-id="57350-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="57350-124">La tarjeta de red no es compatible con el modo promiscuo, lo que significa que solo capturará el tráfico que se difunde por naturaleza o solo implica el equipo local.</span><span class="sxs-lookup"><span data-stu-id="57350-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="57350-125"><dt>**NETWORKINFO \_ marca \_ ras**</dt></span><span class="sxs-lookup"><span data-stu-id="57350-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="57350-126">Se trata de una tarjeta de red virtual que es una conexión RAS (servidor de acceso remoto) a través de un módem u otra tarjeta de red.</span><span class="sxs-lookup"><span data-stu-id="57350-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="57350-127"><dt>**\_ \_ tarjeta remota de marcas de NETWORKINFO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="57350-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="57350-128">La tarjeta de red no está en el equipo local, pero está realizando la captura en un equipo remoto en el Bequest del equipo local.</span><span class="sxs-lookup"><span data-stu-id="57350-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="57350-129"><dt>**NETWORKINFO \_ marca \_ el \_ nal remoto**</dt></span><span class="sxs-lookup"><span data-stu-id="57350-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="57350-130">Obsoleto No use.</span><span class="sxs-lookup"><span data-stu-id="57350-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="57350-131"><dt>**NETWORKINFO \_ marcas de acceso \_ remoto de \_ nal \_ conectadas**</dt></span><span class="sxs-lookup"><span data-stu-id="57350-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="57350-132">Obsoleto No use.</span><span class="sxs-lookup"><span data-stu-id="57350-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="57350-133">**TimestampScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="57350-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="57350-134">Por ejemplo, un valor de 1 indica 1/1 MS, 10 indica 1/10 ms, 100 indica 1/100 MS, etc.</span><span class="sxs-lookup"><span data-stu-id="57350-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="57350-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="57350-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="57350-136">Nombre de la estación de trabajo remota.</span><span class="sxs-lookup"><span data-stu-id="57350-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="57350-137">**PModeSupported**</span><span class="sxs-lookup"><span data-stu-id="57350-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="57350-138">Indicador de compatibilidad de modo P de NIC.</span><span class="sxs-lookup"><span data-stu-id="57350-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="57350-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="57350-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="57350-140">Campo de comentario del adaptador.</span><span class="sxs-lookup"><span data-stu-id="57350-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57350-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57350-141">Requirements</span></span>



| <span data-ttu-id="57350-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="57350-142">Requirement</span></span> | <span data-ttu-id="57350-143">Value</span><span class="sxs-lookup"><span data-stu-id="57350-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="57350-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57350-144">Minimum supported client</span></span><br/> | <span data-ttu-id="57350-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="57350-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="57350-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57350-146">Minimum supported server</span></span><br/> | <span data-ttu-id="57350-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="57350-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="57350-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57350-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="57350-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="57350-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 




