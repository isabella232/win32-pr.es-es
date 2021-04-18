---
description: El método SetAddressInfo establece la información de dirección.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'ITConnection:: SetAddressInfo (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690200"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="1222e-103">ITConnection:: SetAddressInfo (método)</span><span class="sxs-lookup"><span data-stu-id="1222e-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="1222e-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1222e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1222e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="1222e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1222e-106">El método **SetAddressInfo** establece la información de dirección.</span><span class="sxs-lookup"><span data-stu-id="1222e-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1222e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1222e-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="1222e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1222e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1222e-109">*pStartAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1222e-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1222e-110">Puntero a un **BSTR** que contiene la dirección de inicio.</span><span class="sxs-lookup"><span data-stu-id="1222e-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="1222e-111">*NumAddresses* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1222e-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1222e-112">Número de direcciones que se usarán para la sesión.</span><span class="sxs-lookup"><span data-stu-id="1222e-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="1222e-113">*TTL* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1222e-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1222e-114">ámbito del [*período*](t-tapgloss.md) de vida (TTL) para las transmisiones en las direcciones.</span><span class="sxs-lookup"><span data-stu-id="1222e-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1222e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1222e-115">Return value</span></span>

<span data-ttu-id="1222e-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1222e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="1222e-117">Value</span><span class="sxs-lookup"><span data-stu-id="1222e-117">Value</span></span>                                                                                         | <span data-ttu-id="1222e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="1222e-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1222e-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1222e-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1222e-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1222e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1222e-122">El parámetro *pStartAddress*, *NumAddresses* o *TTL* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1222e-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="1222e-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1222e-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1222e-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="1222e-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1222e-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="1222e-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="1222e-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1222e-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="1222e-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="1222e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1222e-129">Remarks</span></span>

<span data-ttu-id="1222e-130">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PStartAddress* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="1222e-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1222e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1222e-131">Requirements</span></span>



| <span data-ttu-id="1222e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1222e-132">Requirement</span></span> | <span data-ttu-id="1222e-133">Value</span><span class="sxs-lookup"><span data-stu-id="1222e-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1222e-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="1222e-134">TAPI version</span></span><br/> | <span data-ttu-id="1222e-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1222e-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1222e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1222e-136">Header</span></span><br/>       | <dl> <span data-ttu-id="1222e-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1222e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1222e-138">Library</span></span><br/>      | <dl> <span data-ttu-id="1222e-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1222e-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1222e-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="1222e-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1222e-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1222e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1222e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1222e-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="1222e-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

