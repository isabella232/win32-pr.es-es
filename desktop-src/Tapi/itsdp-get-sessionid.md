---
description: El \_ método get SessionID obtiene el valor de NTP de 32 bits (Protocolo de tiempo de red) que actúa como identificador de sesión. Se genera automáticamente cuando se crea la sesión.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Método ITSdp:: get_SessionId (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690332"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="a8323-104">ITSdp:: get \_ SessionID (método)</span><span class="sxs-lookup"><span data-stu-id="a8323-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="a8323-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a8323-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a8323-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a8323-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a8323-107">El método **Get \_ SessionID** obtiene el valor de NTP de 32 bits (Protocolo de tiempo de red) que actúa como identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8323-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="a8323-108">Se genera automáticamente cuando se crea la sesión.</span><span class="sxs-lookup"><span data-stu-id="a8323-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8323-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8323-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="a8323-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8323-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8323-111">*pSessionId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a8323-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8323-112">Puntero al identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8323-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8323-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8323-113">Return value</span></span>

<span data-ttu-id="a8323-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a8323-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a8323-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a8323-115">Return code</span></span>                                                                                   | <span data-ttu-id="a8323-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8323-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a8323-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a8323-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8323-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a8323-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a8323-120">El parámetro *pSessionId* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a8323-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="a8323-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a8323-122">El parámetro *pSessionId* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="a8323-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="a8323-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a8323-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a8323-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a8323-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a8323-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a8323-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a8323-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a8323-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="a8323-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a8323-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8323-129">Remarks</span></span>

<span data-ttu-id="a8323-130">El valor devuelto de este método podría ser **ULong**, pero Visual Basic no admite el tipo **ULong** .</span><span class="sxs-lookup"><span data-stu-id="a8323-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="a8323-131">Un **valor Double** es el siguiente tipo más pequeño que abarca todo el intervalo de valores requerido.</span><span class="sxs-lookup"><span data-stu-id="a8323-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8323-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8323-132">Requirements</span></span>



| <span data-ttu-id="a8323-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8323-133">Requirement</span></span> | <span data-ttu-id="a8323-134">Value</span><span class="sxs-lookup"><span data-stu-id="a8323-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8323-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a8323-135">TAPI version</span></span><br/> | <span data-ttu-id="a8323-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a8323-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a8323-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8323-137">Header</span></span><br/>       | <dl> <span data-ttu-id="a8323-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8323-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8323-139">Library</span></span><br/>      | <dl> <span data-ttu-id="a8323-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a8323-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8323-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="a8323-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8323-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8323-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8323-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8323-144">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a8323-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




