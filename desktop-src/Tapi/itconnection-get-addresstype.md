---
description: El \_ método get AddressType obtiene el tipo de dirección.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'Método ITConnection:: get_AddressType (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680204"
---
# <a name="itconnectionget_addresstype-method"></a><span data-ttu-id="235e8-103">ITConnection:: get \_ AddressType (método)</span><span class="sxs-lookup"><span data-stu-id="235e8-103">ITConnection::get\_AddressType method</span></span>

<span data-ttu-id="235e8-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="235e8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="235e8-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="235e8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="235e8-106">El método **Get \_ AddressType** obtiene el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="235e8-106">The **get\_AddressType** method gets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="235e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="235e8-107">Syntax</span></span>


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="235e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="235e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235e8-109">*ppAddressType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="235e8-109">*ppAddressType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="235e8-110">Puntero a un **BSTR** que contiene el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="235e8-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235e8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="235e8-111">Return value</span></span>

<span data-ttu-id="235e8-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="235e8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="235e8-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="235e8-113">Return code</span></span>                                                                                   | <span data-ttu-id="235e8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="235e8-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="235e8-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="235e8-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="235e8-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="235e8-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="235e8-118">El parámetro *ppAddressType* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="235e8-118">The *ppAddressType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="235e8-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="235e8-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="235e8-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="235e8-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="235e8-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="235e8-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="235e8-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="235e8-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="235e8-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="235e8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="235e8-125">Remarks</span></span>

<span data-ttu-id="235e8-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppAddressType* .</span><span class="sxs-lookup"><span data-stu-id="235e8-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppAddressType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="235e8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="235e8-127">Requirements</span></span>



| <span data-ttu-id="235e8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="235e8-128">Requirement</span></span> | <span data-ttu-id="235e8-129">Value</span><span class="sxs-lookup"><span data-stu-id="235e8-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="235e8-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="235e8-130">TAPI version</span></span><br/> | <span data-ttu-id="235e8-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="235e8-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="235e8-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="235e8-132">Header</span></span><br/>       | <dl> <span data-ttu-id="235e8-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="235e8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="235e8-134">Library</span></span><br/>      | <dl> <span data-ttu-id="235e8-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="235e8-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="235e8-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="235e8-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235e8-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235e8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="235e8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235e8-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="235e8-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="235e8-140">**ITConnection::p \_ AddressType AddressType**</span><span class="sxs-lookup"><span data-stu-id="235e8-140">**ITConnection::put\_AddressType**</span></span>](itconnection-put-addresstype.md)
</dt> </dl>

 

