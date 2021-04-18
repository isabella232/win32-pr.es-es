---
description: El \_ método get StartAddress obtiene la primera dirección que se va a utilizar para la sesión.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Método ITConnection:: get_StartAddress (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690206"
---
# <a name="itconnectionget_startaddress-method"></a><span data-ttu-id="f6095-103">ITConnection:: get \_ StartAddress (método)</span><span class="sxs-lookup"><span data-stu-id="f6095-103">ITConnection::get\_StartAddress method</span></span>

<span data-ttu-id="f6095-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f6095-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6095-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f6095-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6095-106">El método **Get \_ StartAddress** obtiene la primera dirección que se va a utilizar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="f6095-106">The **get\_StartAddress** method gets the first address to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6095-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6095-107">Syntax</span></span>


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a><span data-ttu-id="f6095-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6095-109">*ppStartAddress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6095-109">*ppStartAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6095-110">Puntero a un **BSTR** que contiene la dirección de inicio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f6095-110">Pointer to a **BSTR** containing the starting address for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6095-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6095-111">Return value</span></span>

<span data-ttu-id="f6095-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f6095-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f6095-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f6095-113">Return code</span></span>                                                                                   | <span data-ttu-id="f6095-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6095-114">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6095-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f6095-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6095-116">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f6095-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f6095-118">El parámetro *ppStartAddress* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f6095-118">The *ppStartAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f6095-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f6095-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f6095-120">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="f6095-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f6095-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f6095-122">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f6095-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f6095-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="f6095-124">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f6095-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6095-125">Remarks</span></span>

<span data-ttu-id="f6095-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppStartAddress* .</span><span class="sxs-lookup"><span data-stu-id="f6095-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppStartAddress* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6095-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6095-127">Requirements</span></span>



| <span data-ttu-id="f6095-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6095-128">Requirement</span></span> | <span data-ttu-id="f6095-129">Value</span><span class="sxs-lookup"><span data-stu-id="f6095-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6095-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f6095-130">TAPI version</span></span><br/> | <span data-ttu-id="f6095-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f6095-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f6095-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6095-132">Header</span></span><br/>       | <dl> <span data-ttu-id="f6095-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6095-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6095-134">Library</span></span><br/>      | <dl> <span data-ttu-id="f6095-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f6095-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6095-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6095-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6095-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6095-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6095-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6095-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="f6095-139">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

