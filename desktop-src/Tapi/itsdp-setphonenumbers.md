---
description: El método SetPhoneNumbers establece una matriz de números de teléfono asociados a un BLOB de conferencia.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'ITSdp:: SetPhoneNumbers (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680451"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="69ee5-103">ITSdp:: SetPhoneNumbers (método)</span><span class="sxs-lookup"><span data-stu-id="69ee5-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="69ee5-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69ee5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="69ee5-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="69ee5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="69ee5-106">El método **SetPhoneNumbers** establece una matriz de números de teléfono asociados a un BLOB de conferencia.</span><span class="sxs-lookup"><span data-stu-id="69ee5-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ee5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69ee5-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="69ee5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69ee5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ee5-109">*Números* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="69ee5-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69ee5-110">SAFEARRAY de **BSTR** s enumerando números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="69ee5-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="69ee5-111">*Nombres* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="69ee5-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69ee5-112">SAFEARRAY de nombres de lista **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="69ee5-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ee5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69ee5-113">Return value</span></span>

<span data-ttu-id="69ee5-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="69ee5-114">This method can return one of these values.</span></span>



| <span data-ttu-id="69ee5-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="69ee5-115">Return code</span></span>                                                                                   | <span data-ttu-id="69ee5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ee5-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="69ee5-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="69ee5-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="69ee5-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="69ee5-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="69ee5-120">El parámetro *numbers* o *names* no es válido.</span><span class="sxs-lookup"><span data-stu-id="69ee5-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="69ee5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="69ee5-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="69ee5-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="69ee5-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="69ee5-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="69ee5-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="69ee5-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="69ee5-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="69ee5-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="69ee5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69ee5-127">Remarks</span></span>

<span data-ttu-id="69ee5-128">Las listas a las que apuntan los *números* y *los nombres* tienen la misma longitud.</span><span class="sxs-lookup"><span data-stu-id="69ee5-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ee5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ee5-129">Requirements</span></span>



| <span data-ttu-id="69ee5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ee5-130">Requirement</span></span> | <span data-ttu-id="69ee5-131">Value</span><span class="sxs-lookup"><span data-stu-id="69ee5-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69ee5-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="69ee5-132">TAPI version</span></span><br/> | <span data-ttu-id="69ee5-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="69ee5-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="69ee5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69ee5-134">Header</span></span><br/>       | <dl> <span data-ttu-id="69ee5-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="69ee5-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69ee5-136">Library</span></span><br/>      | <dl> <span data-ttu-id="69ee5-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="69ee5-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69ee5-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="69ee5-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69ee5-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ee5-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="69ee5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ee5-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="69ee5-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




