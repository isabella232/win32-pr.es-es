---
description: El \_ método get originador obtiene el autor de la Conferencia.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'Método ITSdp:: get_Originator (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679314"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="f593d-103">ITSdp:: get \_ ORIGINATOR (método)</span><span class="sxs-lookup"><span data-stu-id="f593d-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="f593d-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f593d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f593d-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f593d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f593d-106">El método **Get \_ originador** obtiene el autor de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="f593d-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="f593d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f593d-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="f593d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f593d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f593d-109">*ppOriginator* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f593d-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f593d-110">Puntero a una representación **BSTR** del autor de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="f593d-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f593d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f593d-111">Return value</span></span>

<span data-ttu-id="f593d-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f593d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f593d-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f593d-113">Return code</span></span>                                                                                   | <span data-ttu-id="f593d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f593d-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f593d-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f593d-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f593d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f593d-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f593d-118">El parámetro *ppOriginator* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f593d-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f593d-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f593d-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f593d-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f593d-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f593d-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f593d-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f593d-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f593d-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f593d-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f593d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f593d-125">Remarks</span></span>

<span data-ttu-id="f593d-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppOriginator* .</span><span class="sxs-lookup"><span data-stu-id="f593d-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f593d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f593d-127">Requirements</span></span>



| <span data-ttu-id="f593d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f593d-128">Requirement</span></span> | <span data-ttu-id="f593d-129">Value</span><span class="sxs-lookup"><span data-stu-id="f593d-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f593d-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f593d-130">TAPI version</span></span><br/> | <span data-ttu-id="f593d-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f593d-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f593d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f593d-132">Header</span></span><br/>       | <dl> <span data-ttu-id="f593d-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f593d-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f593d-134">Library</span></span><br/>      | <dl> <span data-ttu-id="f593d-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f593d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f593d-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="f593d-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f593d-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f593d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f593d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f593d-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f593d-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="f593d-140">**ITSdp: originador de:p UT \_**</span><span class="sxs-lookup"><span data-stu-id="f593d-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

