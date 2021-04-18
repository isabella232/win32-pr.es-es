---
description: El \_ método get SessionVersion obtiene el valor de 32 bits (idealmente, el protocolo de tiempo de red o NTP) que sirve como versión de sesión.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Método ITSdp:: get_SessionVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681297"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="f1b0a-103">ITSdp:: get \_ SessionVersion (método)</span><span class="sxs-lookup"><span data-stu-id="f1b0a-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="f1b0a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1b0a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f1b0a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f1b0a-106">El método **Get \_ SessionVersion** obtiene el valor de 32 bits (idealmente, el protocolo de tiempo de red o NTP) que sirve como versión de sesión.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="f1b0a-107">Aunque esto se genera automáticamente cuando se crea la sesión, el usuario es responsable de cambiarla cuando se modifica SDP.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b0a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1b0a-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="f1b0a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1b0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b0a-110">*pSessionVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f1b0a-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1b0a-111">Puntero al identificador de la versión de sesión.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b0a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b0a-112">Return value</span></span>

<span data-ttu-id="f1b0a-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f1b0a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f1b0a-114">Return code</span></span>                                                                                   | <span data-ttu-id="f1b0a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1b0a-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1b0a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1b0a-117">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="f1b0a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f1b0a-119">El parámetro *pSessionVersion* no es válido.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="f1b0a-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f1b0a-121">El parámetro *pSessionVersion* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f1b0a-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1b0a-123">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="f1b0a-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f1b0a-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f1b0a-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f1b0a-127">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="f1b0a-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1b0a-128">Remarks</span></span>

<span data-ttu-id="f1b0a-129">El valor devuelto de este método podría ser **ULong**, pero Visual Basic no admite el tipo **ULong** .</span><span class="sxs-lookup"><span data-stu-id="f1b0a-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="f1b0a-130">Un **valor Double** es el siguiente tipo más pequeño que abarca todo el intervalo de valores requerido.</span><span class="sxs-lookup"><span data-stu-id="f1b0a-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b0a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b0a-131">Requirements</span></span>



| <span data-ttu-id="f1b0a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b0a-132">Requirement</span></span> | <span data-ttu-id="f1b0a-133">Value</span><span class="sxs-lookup"><span data-stu-id="f1b0a-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b0a-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f1b0a-134">TAPI version</span></span><br/> | <span data-ttu-id="f1b0a-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f1b0a-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f1b0a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1b0a-136">Header</span></span><br/>       | <dl> <span data-ttu-id="f1b0a-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1b0a-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1b0a-138">Library</span></span><br/>      | <dl> <span data-ttu-id="f1b0a-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f1b0a-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1b0a-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="f1b0a-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1b0a-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b0a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1b0a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b0a-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f1b0a-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="f1b0a-144">**ITSdp::p UT \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="f1b0a-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




