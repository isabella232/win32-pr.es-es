---
description: El \_ método get Bandwidth obtiene el valor de ancho de banda.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: 'Método ITConnection:: get_Bandwidth (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ff4d5902a3434839167ffd28fad2b7552e5c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691053"
---
# <a name="itconnectionget_bandwidth-method"></a><span data-ttu-id="f1b28-103">ITConnection:: get \_ Bandwidth (método)</span><span class="sxs-lookup"><span data-stu-id="f1b28-103">ITConnection::get\_Bandwidth method</span></span>

<span data-ttu-id="f1b28-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1b28-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1b28-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f1b28-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f1b28-106">El método **Get \_ Bandwidth** obtiene el valor de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="f1b28-106">The **get\_Bandwidth** method gets the bandwidth value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b28-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1b28-107">Syntax</span></span>


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="f1b28-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1b28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b28-109">*pBandwidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f1b28-109">*pBandwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b28-110">Valor de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="f1b28-110">Bandwidth value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b28-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b28-111">Return value</span></span>

<span data-ttu-id="f1b28-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f1b28-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f1b28-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b28-113">Return code</span></span>                                                                                   | <span data-ttu-id="f1b28-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1b28-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f1b28-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1b28-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1b28-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f1b28-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f1b28-118">El parámetro *pBandwidth* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f1b28-118">The *pBandwidth* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="f1b28-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1b28-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f1b28-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f1b28-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f1b28-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f1b28-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f1b28-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f1b28-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f1b28-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f1b28-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b28-125">Requirements</span></span>



| <span data-ttu-id="f1b28-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b28-126">Requirement</span></span> | <span data-ttu-id="f1b28-127">Value</span><span class="sxs-lookup"><span data-stu-id="f1b28-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b28-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f1b28-128">TAPI version</span></span><br/> | <span data-ttu-id="f1b28-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f1b28-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f1b28-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1b28-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f1b28-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1b28-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1b28-132">Library</span></span><br/>      | <dl> <span data-ttu-id="f1b28-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f1b28-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1b28-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="f1b28-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1b28-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b28-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1b28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b28-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="f1b28-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




