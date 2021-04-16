---
description: El \_ método put AddressType establece el tipo de dirección.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: 'ITConnection: método de ut_AddressType de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679319"
---
# <a name="itconnectionput_addresstype-method"></a><span data-ttu-id="0bed6-103">ITConnection::p \_ método UT AddressType</span><span class="sxs-lookup"><span data-stu-id="0bed6-103">ITConnection::put\_AddressType method</span></span>

<span data-ttu-id="0bed6-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0bed6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0bed6-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0bed6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0bed6-106">El método **Put \_ AddressType** establece el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="0bed6-106">The **put\_AddressType** method sets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bed6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bed6-107">Syntax</span></span>


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="0bed6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bed6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bed6-109">*pAddressType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0bed6-109">*pAddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bed6-110">Puntero a un **BSTR** que contiene el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="0bed6-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bed6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bed6-111">Return value</span></span>

<span data-ttu-id="0bed6-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0bed6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0bed6-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0bed6-113">Return code</span></span>                                                                                   | <span data-ttu-id="0bed6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bed6-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0bed6-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0bed6-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0bed6-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0bed6-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0bed6-118">El parámetro *pAddressType* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0bed6-118">The *pAddressType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="0bed6-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0bed6-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0bed6-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0bed6-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0bed6-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="0bed6-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0bed6-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0bed6-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="0bed6-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0bed6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bed6-125">Remarks</span></span>

<span data-ttu-id="0bed6-126">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PAddressType* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="0bed6-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAddressType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bed6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bed6-127">Requirements</span></span>



| <span data-ttu-id="0bed6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bed6-128">Requirement</span></span> | <span data-ttu-id="0bed6-129">Value</span><span class="sxs-lookup"><span data-stu-id="0bed6-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bed6-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0bed6-130">TAPI version</span></span><br/> | <span data-ttu-id="0bed6-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0bed6-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0bed6-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bed6-132">Header</span></span><br/>       | <dl> <span data-ttu-id="0bed6-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0bed6-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bed6-134">Library</span></span><br/>      | <dl> <span data-ttu-id="0bed6-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0bed6-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0bed6-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="0bed6-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bed6-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bed6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bed6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bed6-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="0bed6-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="0bed6-140">**ITConnection:: get \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="0bed6-140">**ITConnection::get\_AddressType**</span></span>](itconnection-get-addresstype.md)
</dt> </dl>

 

