---
description: El \_ método get ProtocolVersion obtiene la versión del protocolo del Protocolo de descriptor de sesión (SDP; consulte RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Método ITSdp:: get_ProtocolVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679492"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="b0b5a-103">ITSdp:: get \_ ProtocolVersion (método)</span><span class="sxs-lookup"><span data-stu-id="b0b5a-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="b0b5a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0b5a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b0b5a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b0b5a-106">El método **Get \_ ProtocolVersion** obtiene la versión del protocolo del Protocolo de descriptor de sesión (SDP; consulte RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="b0b5a-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b5a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0b5a-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="b0b5a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0b5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b5a-109">*pProtocolVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b0b5a-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0b5a-110">Puntero a la versión del protocolo.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b5a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0b5a-111">Return value</span></span>

<span data-ttu-id="b0b5a-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b0b5a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b0b5a-113">Return code</span></span>                                                                                   | <span data-ttu-id="b0b5a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0b5a-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0b5a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b0b5a-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b0b5a-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b0b5a-118">El parámetro *pProtocolVersion* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="b0b5a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b0b5a-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="b0b5a-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b0b5a-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="b0b5a-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b0b5a-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="b0b5a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b5a-125">Requirements</span></span>



| <span data-ttu-id="b0b5a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b5a-126">Requirement</span></span> | <span data-ttu-id="b0b5a-127">Value</span><span class="sxs-lookup"><span data-stu-id="b0b5a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b5a-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b0b5a-128">TAPI version</span></span><br/> | <span data-ttu-id="b0b5a-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b0b5a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b0b5a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0b5a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="b0b5a-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0b5a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0b5a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="b0b5a-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b0b5a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0b5a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="b0b5a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b5a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0b5a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b5a-137">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="b0b5a-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




