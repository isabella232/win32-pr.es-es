---
description: El \_ método put ORIGINATOR establece el autor de la Conferencia.
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: 'ITSdp: método de ut_Originator de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506554668e697e9281dc5dc15784fa36f7429d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678873"
---
# <a name="itsdpput_originator-method"></a><span data-ttu-id="68540-103">ITSdp::p método de autor de UT \_</span><span class="sxs-lookup"><span data-stu-id="68540-103">ITSdp::put\_Originator method</span></span>

<span data-ttu-id="68540-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68540-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68540-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="68540-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68540-106">El método **Put \_ ORIGINATOR** establece el autor de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="68540-106">The **put\_Originator** method sets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="68540-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68540-107">Syntax</span></span>


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="68540-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68540-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68540-109">*pOriginator* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68540-109">*pOriginator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68540-110">Puntero a una representación **BSTR** del autor de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="68540-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68540-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68540-111">Return value</span></span>

<span data-ttu-id="68540-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="68540-112">This method can return one of these values.</span></span>



| <span data-ttu-id="68540-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68540-113">Return code</span></span>                                                                                   | <span data-ttu-id="68540-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="68540-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="68540-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="68540-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68540-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="68540-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="68540-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="68540-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="68540-118">El parámetro *pOriginator* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="68540-118">The *pOriginator* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="68540-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="68540-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68540-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="68540-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="68540-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="68540-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="68540-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="68540-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="68540-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="68540-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="68540-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="68540-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="68540-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68540-125">Remarks</span></span>

<span data-ttu-id="68540-126">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *POriginator* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="68540-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pOriginator* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="68540-127">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="68540-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="68540-128">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="68540-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="68540-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68540-129">Requirements</span></span>



| <span data-ttu-id="68540-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="68540-130">Requirement</span></span> | <span data-ttu-id="68540-131">Value</span><span class="sxs-lookup"><span data-stu-id="68540-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68540-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="68540-132">TAPI version</span></span><br/> | <span data-ttu-id="68540-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="68540-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="68540-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68540-134">Header</span></span><br/>       | <dl> <span data-ttu-id="68540-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="68540-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="68540-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68540-136">Library</span></span><br/>      | <dl> <span data-ttu-id="68540-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68540-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="68540-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68540-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="68540-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68540-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68540-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="68540-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68540-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="68540-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="68540-142">**ITSdp:: get \_ ORIGINATOR**</span><span class="sxs-lookup"><span data-stu-id="68540-142">**ITSdp::get\_Originator**</span></span>](itsdp-get-originator.md)
</dt> </dl>

 

