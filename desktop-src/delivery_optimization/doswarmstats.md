---
title: Estructura DOSwarmStats (Deliveryoptimization. h)
description: Contiene campos para las estadísticas de descarga y carga de un archivo.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Estructura DOSwarmStats
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714646"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="4903d-104">Estructura DOSwarmStats</span><span class="sxs-lookup"><span data-stu-id="4903d-104">DOSwarmStats structure</span></span>

<span data-ttu-id="4903d-105">Contiene campos para las estadísticas de descarga y carga de un archivo.</span><span class="sxs-lookup"><span data-stu-id="4903d-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4903d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4903d-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="4903d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4903d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4903d-108">**ID**</span><span class="sxs-lookup"><span data-stu-id="4903d-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-109">Cadena terminada en null que se especificó con la llamada a **AddFileWithRanges** .</span><span class="sxs-lookup"><span data-stu-id="4903d-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-110">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="4903d-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-111">Cadena terminada en null que contiene el nombre del archivo en el servidor (por ejemplo, https:// &lt; ruta de acceso del servidor &gt; / &lt; &gt; /file.ext).</span><span class="sxs-lookup"><span data-stu-id="4903d-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="4903d-112">**fileSize**</span><span class="sxs-lookup"><span data-stu-id="4903d-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-113">Tamaño del archivo en bytes.</span><span class="sxs-lookup"><span data-stu-id="4903d-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-114">**totalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="4903d-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-115">Número total de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="4903d-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-116">**bytesFromLanPeers**</span><span class="sxs-lookup"><span data-stu-id="4903d-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-117">Número de bytes transferidos desde los pares de LAN.</span><span class="sxs-lookup"><span data-stu-id="4903d-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-118">**bytesFromGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="4903d-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-119">Número de bytes transferidos desde grupos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="4903d-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-120">**bytesFromInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="4903d-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-121">Número de bytes transferidos desde los pares de Internet.</span><span class="sxs-lookup"><span data-stu-id="4903d-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-122">**bytesFromHttp**</span><span class="sxs-lookup"><span data-stu-id="4903d-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-123">Número de bytes transferidos desde http.</span><span class="sxs-lookup"><span data-stu-id="4903d-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-124">**bytesFromDoinc**</span><span class="sxs-lookup"><span data-stu-id="4903d-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-125">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4903d-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-126">**bytesToLanPeers**</span><span class="sxs-lookup"><span data-stu-id="4903d-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-127">Número de bytes transferidos a los pares de LAN.</span><span class="sxs-lookup"><span data-stu-id="4903d-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-128">**bytesToGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="4903d-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-129">Número de bytes transferidos al grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="4903d-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-130">**bytesToInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="4903d-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-131">Número de bytes transferidos a los pares de Internet.</span><span class="sxs-lookup"><span data-stu-id="4903d-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-132">**httpConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="4903d-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-133">Recuento de conexiones http.</span><span class="sxs-lookup"><span data-stu-id="4903d-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-134">**doincConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="4903d-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-135">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4903d-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-136">**lanConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="4903d-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-137">Recuento de conexiones LAN.</span><span class="sxs-lookup"><span data-stu-id="4903d-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-138">**groupConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="4903d-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-139">Recuento de conexiones de grupo.</span><span class="sxs-lookup"><span data-stu-id="4903d-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-140">**internetConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="4903d-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-141">Recuento de conexiones a Internet.</span><span class="sxs-lookup"><span data-stu-id="4903d-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-142">**downloadDuration**</span><span class="sxs-lookup"><span data-stu-id="4903d-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-143">Duración de la transferencia de archivo en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4903d-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="4903d-144">**downloadMode**</span><span class="sxs-lookup"><span data-stu-id="4903d-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-145">El modo de descarga usado, vea [**DownloadMode**](downloadmode.md).</span><span class="sxs-lookup"><span data-stu-id="4903d-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="4903d-146">**status**</span><span class="sxs-lookup"><span data-stu-id="4903d-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-147">El estado de una transferencia de archivos, vea [**SwarmStatus**](swarmstatus.md).</span><span class="sxs-lookup"><span data-stu-id="4903d-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="4903d-148">**isBackground**</span><span class="sxs-lookup"><span data-stu-id="4903d-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="4903d-149">True, si se trata de una transferencia en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4903d-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4903d-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4903d-150">Requirements</span></span>



| <span data-ttu-id="4903d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="4903d-151">Requirement</span></span> | <span data-ttu-id="4903d-152">Value</span><span class="sxs-lookup"><span data-stu-id="4903d-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4903d-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4903d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="4903d-154">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="4903d-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4903d-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4903d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="4903d-156">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="4903d-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4903d-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4903d-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="4903d-158"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4903d-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





