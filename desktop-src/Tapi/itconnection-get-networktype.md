---
description: El \_ método get NetworkType obtiene el tipo de red.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Método ITConnection:: get_NetworkType (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31189ec0e3b42e3ed249cd0c62365b1f8c793908
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690209"
---
# <a name="itconnectionget_networktype-method"></a><span data-ttu-id="44de7-103">ITConnection:: get \_ NetworkType (método)</span><span class="sxs-lookup"><span data-stu-id="44de7-103">ITConnection::get\_NetworkType method</span></span>

<span data-ttu-id="44de7-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="44de7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="44de7-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="44de7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="44de7-106">El método **Get \_ NetworkType** obtiene el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="44de7-106">The **get\_NetworkType** method gets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="44de7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44de7-107">Syntax</span></span>


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="44de7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44de7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44de7-109">*ppNetworkType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="44de7-109">*ppNetworkType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44de7-110">Puntero a un **BSTR** que contiene el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="44de7-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44de7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44de7-111">Return value</span></span>

<span data-ttu-id="44de7-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="44de7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="44de7-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="44de7-113">Return code</span></span>                                                                                   | <span data-ttu-id="44de7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="44de7-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="44de7-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="44de7-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="44de7-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="44de7-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="44de7-118">El parámetro *ppNetworkType* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="44de7-118">The *ppNetworkType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="44de7-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="44de7-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="44de7-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="44de7-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="44de7-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="44de7-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="44de7-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="44de7-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="44de7-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="44de7-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44de7-125">Remarks</span></span>

<span data-ttu-id="44de7-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppNetworkType* .</span><span class="sxs-lookup"><span data-stu-id="44de7-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppNetworkType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="44de7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44de7-127">Requirements</span></span>



| <span data-ttu-id="44de7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="44de7-128">Requirement</span></span> | <span data-ttu-id="44de7-129">Value</span><span class="sxs-lookup"><span data-stu-id="44de7-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44de7-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="44de7-130">TAPI version</span></span><br/> | <span data-ttu-id="44de7-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="44de7-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="44de7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44de7-132">Header</span></span><br/>       | <dl> <span data-ttu-id="44de7-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="44de7-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44de7-134">Library</span></span><br/>      | <dl> <span data-ttu-id="44de7-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="44de7-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44de7-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="44de7-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44de7-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44de7-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="44de7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44de7-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="44de7-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="44de7-140">**ITConnection::p UT \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="44de7-140">**ITConnection::put\_NetworkType**</span></span>](itconnection-put-networktype.md)
</dt> </dl>

 

