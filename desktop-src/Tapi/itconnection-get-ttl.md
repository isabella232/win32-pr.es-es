---
description: El \_ método get TTL obtiene el ámbito del período de vida (TTL) para las transmisiones en las direcciones.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'Método ITConnection:: get_Ttl (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679320"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="79951-103">ITConnection:: get \_ TTL (método)</span><span class="sxs-lookup"><span data-stu-id="79951-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="79951-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="79951-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="79951-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="79951-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="79951-106">El método **Get \_ TTL** obtiene el ámbito del [*período*](t-tapgloss.md) de vida (TTL) para las transmisiones en las direcciones.</span><span class="sxs-lookup"><span data-stu-id="79951-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="79951-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79951-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="79951-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79951-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79951-109">*pTtl* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79951-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79951-110">Ámbito de TTL.</span><span class="sxs-lookup"><span data-stu-id="79951-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79951-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79951-111">Return value</span></span>

<span data-ttu-id="79951-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="79951-112">This method can return one of these values.</span></span>



| <span data-ttu-id="79951-113">Value</span><span class="sxs-lookup"><span data-stu-id="79951-113">Value</span></span>                                                                                         | <span data-ttu-id="79951-114">Significado</span><span class="sxs-lookup"><span data-stu-id="79951-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="79951-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="79951-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="79951-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="79951-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79951-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="79951-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="79951-118">El parámetro *pTtl* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="79951-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="79951-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="79951-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="79951-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="79951-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="79951-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="79951-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="79951-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="79951-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="79951-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="79951-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="79951-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="79951-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="79951-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79951-125">Requirements</span></span>



| <span data-ttu-id="79951-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="79951-126">Requirement</span></span> | <span data-ttu-id="79951-127">Value</span><span class="sxs-lookup"><span data-stu-id="79951-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79951-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="79951-128">TAPI version</span></span><br/> | <span data-ttu-id="79951-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="79951-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="79951-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79951-130">Header</span></span><br/>       | <dl> <span data-ttu-id="79951-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="79951-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="79951-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79951-132">Library</span></span><br/>      | <dl> <span data-ttu-id="79951-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79951-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="79951-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79951-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="79951-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79951-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79951-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="79951-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79951-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="79951-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




