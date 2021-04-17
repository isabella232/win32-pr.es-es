---
description: El método SetEmailNames establece una matriz de direcciones de correo electrónico asociadas al BLOB de la Conferencia.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'ITSdp:: SetEmailNames (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690526"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="1062f-103">ITSdp:: SetEmailNames (método)</span><span class="sxs-lookup"><span data-stu-id="1062f-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="1062f-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1062f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1062f-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="1062f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1062f-106">El método **SetEmailNames** establece una matriz de direcciones de correo electrónico asociadas al BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="1062f-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="1062f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1062f-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="1062f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1062f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1062f-109">*Direcciones* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1062f-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1062f-110">SAFEARRAY de **BSTR** s enumerando direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1062f-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="1062f-111">*Nombres* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1062f-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1062f-112">SAFEARRAY de nombres de lista **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="1062f-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1062f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1062f-113">Return value</span></span>

<span data-ttu-id="1062f-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1062f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1062f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1062f-115">Return code</span></span>                                                                                   | <span data-ttu-id="1062f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1062f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1062f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1062f-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1062f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1062f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1062f-120">El parámetro *Addresses* o *names* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1062f-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="1062f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1062f-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1062f-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1062f-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1062f-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="1062f-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1062f-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1062f-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="1062f-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1062f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1062f-127">Remarks</span></span>

<span data-ttu-id="1062f-128">Las listas a *las que* apuntan los *nombres* y tienen la misma longitud.</span><span class="sxs-lookup"><span data-stu-id="1062f-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="1062f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1062f-129">Requirements</span></span>



| <span data-ttu-id="1062f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1062f-130">Requirement</span></span> | <span data-ttu-id="1062f-131">Value</span><span class="sxs-lookup"><span data-stu-id="1062f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1062f-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="1062f-132">TAPI version</span></span><br/> | <span data-ttu-id="1062f-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1062f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1062f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1062f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1062f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1062f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1062f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1062f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1062f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1062f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1062f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1062f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1062f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1062f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1062f-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="1062f-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




