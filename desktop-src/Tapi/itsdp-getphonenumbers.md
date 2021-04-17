---
description: El método GetPhoneNumbers obtiene una matriz de números de teléfono asociados a un BLOB de conferencia.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'ITSdp:: GetPhoneNumbers (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681082"
---
# <a name="itsdpgetphonenumbers-method"></a><span data-ttu-id="96508-103">ITSdp:: GetPhoneNumbers (método)</span><span class="sxs-lookup"><span data-stu-id="96508-103">ITSdp::GetPhoneNumbers method</span></span>

<span data-ttu-id="96508-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96508-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="96508-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="96508-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="96508-106">El método **GetPhoneNumbers** obtiene una matriz de números de teléfono asociados a un BLOB de conferencia.</span><span class="sxs-lookup"><span data-stu-id="96508-106">The **GetPhoneNumbers** method gets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="96508-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96508-107">Syntax</span></span>


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="96508-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96508-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96508-109">*pNumbers* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96508-109">*pNumbers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96508-110">Puntero **Variant** a una matriz SafeArray de **BSTR** s que enumera los números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="96508-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="96508-111">*pNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96508-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96508-112">Puntero **Variant** a una matriz SafeArray de nombres de lista **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="96508-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96508-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96508-113">Return value</span></span>

<span data-ttu-id="96508-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="96508-114">This method can return one of these values.</span></span>



| <span data-ttu-id="96508-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="96508-115">Return code</span></span>                                                                                   | <span data-ttu-id="96508-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="96508-116">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96508-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="96508-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="96508-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="96508-118">Method succeeded.</span></span><br/>                                            |
| <dl> <span data-ttu-id="96508-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="96508-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="96508-120">El parámetro *pNumbers* o *pNames* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="96508-120">The *pNumbers* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="96508-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="96508-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="96508-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="96508-122">Insufficient memory exists to perform the operation.</span></span><br/>         |
| <dl> <span data-ttu-id="96508-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="96508-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="96508-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="96508-124">Unspecified error.</span></span><br/>                                           |
| <dl> <span data-ttu-id="96508-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="96508-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="96508-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="96508-126">This method is not yet implemented.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="96508-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96508-127">Remarks</span></span>

<span data-ttu-id="96508-128">Las listas a las que apuntan *pNumbers* y *pNames* tienen la misma longitud.</span><span class="sxs-lookup"><span data-stu-id="96508-128">The lists that *pNumbers* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="96508-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96508-129">Requirements</span></span>



| <span data-ttu-id="96508-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="96508-130">Requirement</span></span> | <span data-ttu-id="96508-131">Value</span><span class="sxs-lookup"><span data-stu-id="96508-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96508-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="96508-132">TAPI version</span></span><br/> | <span data-ttu-id="96508-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="96508-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="96508-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96508-134">Header</span></span><br/>       | <dl> <span data-ttu-id="96508-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="96508-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="96508-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96508-136">Library</span></span><br/>      | <dl> <span data-ttu-id="96508-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96508-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="96508-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96508-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="96508-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96508-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96508-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="96508-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96508-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="96508-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




