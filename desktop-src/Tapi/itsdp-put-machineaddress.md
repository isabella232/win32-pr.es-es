---
description: El \_ método put MachineAddress establece la dirección de la máquina del host de origen.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'ITSdp: método de ut_MachineAddress de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681065"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="b5315-103">ITSdp::p \_ método MachineAddress UT</span><span class="sxs-lookup"><span data-stu-id="b5315-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="b5315-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b5315-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5315-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b5315-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b5315-106">El método **Put \_ MachineAddress** establece la dirección de la máquina del host de origen.</span><span class="sxs-lookup"><span data-stu-id="b5315-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5315-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5315-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="b5315-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5315-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5315-109">*pMachineAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5315-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5315-110">Puntero a un **BSTR** que contiene la dirección de la máquina del host de conferencia.</span><span class="sxs-lookup"><span data-stu-id="b5315-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5315-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5315-111">Return value</span></span>

<span data-ttu-id="b5315-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b5315-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b5315-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b5315-113">Return code</span></span>                                                                                   | <span data-ttu-id="b5315-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5315-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5315-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b5315-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b5315-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="b5315-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b5315-118">El parámetro *pMachineAddress* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="b5315-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="b5315-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b5315-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b5315-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="b5315-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b5315-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b5315-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b5315-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b5315-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="b5315-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="b5315-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5315-125">Remarks</span></span>

<span data-ttu-id="b5315-126">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PMachineAddress* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="b5315-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="b5315-127">El parámetro *pMachineAddress* puede ser un nombre DNS ("johnsmith.workinghard.Microsoft.com") o una dirección IP ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="b5315-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="b5315-128">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="b5315-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="b5315-129">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="b5315-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5315-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5315-130">Requirements</span></span>



| <span data-ttu-id="b5315-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5315-131">Requirement</span></span> | <span data-ttu-id="b5315-132">Value</span><span class="sxs-lookup"><span data-stu-id="b5315-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5315-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b5315-133">TAPI version</span></span><br/> | <span data-ttu-id="b5315-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b5315-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b5315-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5315-135">Header</span></span><br/>       | <dl> <span data-ttu-id="b5315-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5315-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5315-137">Library</span></span><br/>      | <dl> <span data-ttu-id="b5315-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b5315-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5315-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="b5315-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5315-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5315-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5315-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5315-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="b5315-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="b5315-143">**ITSdp:: get \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="b5315-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

