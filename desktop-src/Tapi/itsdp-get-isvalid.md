---
description: El \_ método get IsValid valida el BLOB del Protocolo de descriptor de sesión (SDP; consulte RFC 2327) para los valores de estructura y campo.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Método ITSdp:: get_IsValid (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681234"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="f28d3-103">ITSdp:: get \_ IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="f28d3-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="f28d3-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f28d3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f28d3-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f28d3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f28d3-106">El método **Get \_ IsValid** valida el BLOB del Protocolo de descriptor de sesión (SDP; consulte RFC 2327) para los valores de estructura y campo.</span><span class="sxs-lookup"><span data-stu-id="f28d3-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28d3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f28d3-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="f28d3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f28d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f28d3-109">*pfIsValid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f28d3-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f28d3-110">Indica si la estructura del BLOB es válida.</span><span class="sxs-lookup"><span data-stu-id="f28d3-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f28d3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f28d3-111">Return value</span></span>

<span data-ttu-id="f28d3-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f28d3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f28d3-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f28d3-113">Return code</span></span>                                                                                   | <span data-ttu-id="f28d3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28d3-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f28d3-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f28d3-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f28d3-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f28d3-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f28d3-118">El parámetro *pfIsValid* no es válido.</span><span class="sxs-lookup"><span data-stu-id="f28d3-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="f28d3-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f28d3-120">El parámetro *pfIsValid* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f28d3-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="f28d3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f28d3-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f28d3-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f28d3-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f28d3-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f28d3-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f28d3-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f28d3-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f28d3-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f28d3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f28d3-127">Requirements</span></span>



| <span data-ttu-id="f28d3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f28d3-128">Requirement</span></span> | <span data-ttu-id="f28d3-129">Value</span><span class="sxs-lookup"><span data-stu-id="f28d3-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f28d3-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f28d3-130">TAPI version</span></span><br/> | <span data-ttu-id="f28d3-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f28d3-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f28d3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f28d3-132">Header</span></span><br/>       | <dl> <span data-ttu-id="f28d3-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f28d3-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f28d3-134">Library</span></span><br/>      | <dl> <span data-ttu-id="f28d3-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f28d3-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f28d3-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="f28d3-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f28d3-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f28d3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f28d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28d3-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f28d3-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




