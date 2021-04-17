---
description: El \_ método get MachineAddress obtiene la dirección de la máquina del host de origen.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Método ITSdp:: get_MachineAddress (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690196"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="74d2a-103">ITSdp:: get \_ MachineAddress (método)</span><span class="sxs-lookup"><span data-stu-id="74d2a-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="74d2a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="74d2a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="74d2a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="74d2a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="74d2a-106">El método **Get \_ MachineAddress** obtiene la dirección de la máquina del host de origen.</span><span class="sxs-lookup"><span data-stu-id="74d2a-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d2a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74d2a-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="74d2a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74d2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d2a-109">*ppMachineAddress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74d2a-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74d2a-110">Puntero a un **BSTR** que contiene la dirección de la máquina del host de conferencia.</span><span class="sxs-lookup"><span data-stu-id="74d2a-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d2a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74d2a-111">Return value</span></span>

<span data-ttu-id="74d2a-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="74d2a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="74d2a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="74d2a-113">Return code</span></span>                                                                                   | <span data-ttu-id="74d2a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="74d2a-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="74d2a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="74d2a-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="74d2a-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="74d2a-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="74d2a-118">El parámetro *ppMachineAddres* s no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="74d2a-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="74d2a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="74d2a-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="74d2a-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="74d2a-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="74d2a-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="74d2a-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="74d2a-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="74d2a-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="74d2a-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="74d2a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74d2a-125">Remarks</span></span>

<span data-ttu-id="74d2a-126">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppMachineAddress* .</span><span class="sxs-lookup"><span data-stu-id="74d2a-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="74d2a-127">El parámetro *ppMachineAddress* se puede devolver como un nombre DNS ("johnsmith.workinghard.Microsoft.com") o una dirección IP ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="74d2a-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="74d2a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74d2a-128">Requirements</span></span>



| <span data-ttu-id="74d2a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d2a-129">Requirement</span></span> | <span data-ttu-id="74d2a-130">Value</span><span class="sxs-lookup"><span data-stu-id="74d2a-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74d2a-131">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="74d2a-131">TAPI version</span></span><br/> | <span data-ttu-id="74d2a-132">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="74d2a-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="74d2a-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74d2a-133">Header</span></span><br/>       | <dl> <span data-ttu-id="74d2a-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="74d2a-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74d2a-135">Library</span></span><br/>      | <dl> <span data-ttu-id="74d2a-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="74d2a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74d2a-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="74d2a-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74d2a-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74d2a-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="74d2a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d2a-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="74d2a-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="74d2a-141">**ITSdp::p UT \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="74d2a-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

