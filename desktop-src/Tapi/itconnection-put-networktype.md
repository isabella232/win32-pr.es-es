---
description: El \_ método put NetworkType establece el tipo de red.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: 'ITConnection: método de ut_NetworkType de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690201"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="201fd-103">ITConnection::p \_ método NetworkType UT</span><span class="sxs-lookup"><span data-stu-id="201fd-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="201fd-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="201fd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="201fd-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="201fd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="201fd-106">El método **Put \_ NetworkType** establece el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="201fd-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="201fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="201fd-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="201fd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="201fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="201fd-109">*pNetworkType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="201fd-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="201fd-110">Puntero a un **BSTR** que contiene el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="201fd-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="201fd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="201fd-111">Return value</span></span>

<span data-ttu-id="201fd-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="201fd-112">This method can return one of these values.</span></span>



| <span data-ttu-id="201fd-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="201fd-113">Return code</span></span>                                                                                   | <span data-ttu-id="201fd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="201fd-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="201fd-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="201fd-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="201fd-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="201fd-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="201fd-118">El parámetro *pNetworkType* no es válido.</span><span class="sxs-lookup"><span data-stu-id="201fd-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="201fd-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="201fd-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="201fd-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="201fd-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="201fd-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="201fd-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="201fd-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="201fd-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="201fd-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="201fd-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="201fd-125">Remarks</span></span>

<span data-ttu-id="201fd-126">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PNetworkType* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="201fd-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="201fd-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="201fd-127">Requirements</span></span>



| <span data-ttu-id="201fd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="201fd-128">Requirement</span></span> | <span data-ttu-id="201fd-129">Value</span><span class="sxs-lookup"><span data-stu-id="201fd-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="201fd-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="201fd-130">TAPI version</span></span><br/> | <span data-ttu-id="201fd-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="201fd-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="201fd-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="201fd-132">Header</span></span><br/>       | <dl> <span data-ttu-id="201fd-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="201fd-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="201fd-134">Library</span></span><br/>      | <dl> <span data-ttu-id="201fd-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="201fd-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="201fd-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="201fd-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201fd-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="201fd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="201fd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201fd-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="201fd-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="201fd-140">**ITConnection:: get \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="201fd-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

