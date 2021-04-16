---
description: El método GetEmailNames obtiene una matriz de nombres de correo electrónico asociada al BLOB de la Conferencia.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'ITSdp:: GetEmailNames (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690006"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="e5863-103">ITSdp:: GetEmailNames (método)</span><span class="sxs-lookup"><span data-stu-id="e5863-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="e5863-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e5863-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e5863-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e5863-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e5863-106">El método **GetEmailNames** obtiene una matriz de nombres de correo electrónico asociada al BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="e5863-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5863-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5863-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="e5863-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5863-109">*pAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e5863-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5863-110">Puntero **Variant** a una matriz SafeArray de **BSTR** s que enumera las direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e5863-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="e5863-111">*pNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e5863-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5863-112">Puntero **Variant** a una matriz SafeArray de nombres de lista **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="e5863-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5863-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5863-113">Return value</span></span>

<span data-ttu-id="e5863-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e5863-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e5863-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e5863-115">Return code</span></span>                                                                                   | <span data-ttu-id="e5863-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5863-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5863-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e5863-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5863-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="e5863-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e5863-120">El parámetro *pAddresses* o *pNames* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="e5863-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="e5863-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e5863-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e5863-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="e5863-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e5863-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e5863-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="e5863-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e5863-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="e5863-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="e5863-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5863-127">Remarks</span></span>

<span data-ttu-id="e5863-128">Las listas a las que apuntan *pAddresses* y *pNames* tienen la misma longitud.</span><span class="sxs-lookup"><span data-stu-id="e5863-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5863-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5863-129">Requirements</span></span>



| <span data-ttu-id="e5863-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5863-130">Requirement</span></span> | <span data-ttu-id="e5863-131">Value</span><span class="sxs-lookup"><span data-stu-id="e5863-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5863-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e5863-132">TAPI version</span></span><br/> | <span data-ttu-id="e5863-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e5863-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e5863-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5863-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e5863-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5863-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5863-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e5863-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e5863-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5863-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e5863-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5863-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5863-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5863-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5863-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="e5863-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




