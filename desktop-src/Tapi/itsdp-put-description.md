---
description: El \_ método de Descripción Put establece la descripción de la sesión.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: 'ITSdp: método de ut_Description de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690953"
---
# <a name="itsdpput_description-method"></a><span data-ttu-id="b9ef4-103">ITSdp::p método de descripción de UT \_</span><span class="sxs-lookup"><span data-stu-id="b9ef4-103">ITSdp::put\_Description method</span></span>

<span data-ttu-id="b9ef4-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b9ef4-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b9ef4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b9ef4-106">El método de **\_ Descripción Put** establece la descripción de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-106">The **put\_Description** method sets the session description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ef4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9ef4-107">Syntax</span></span>


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a><span data-ttu-id="b9ef4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9ef4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ef4-109">*pDescription* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9ef4-109">*pDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ef4-110">Puntero a un **BSTR** que contiene la descripción de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-110">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ef4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9ef4-111">Return value</span></span>

<span data-ttu-id="b9ef4-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b9ef4-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b9ef4-113">Return code</span></span>                                                                                   | <span data-ttu-id="b9ef4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9ef4-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b9ef4-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b9ef4-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b9ef4-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b9ef4-118">El parámetro *pDescription* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-118">The *pDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="b9ef4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b9ef4-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b9ef4-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b9ef4-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b9ef4-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b9ef4-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b9ef4-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9ef4-125">Remarks</span></span>

<span data-ttu-id="b9ef4-126">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PDescription* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pDescription* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="b9ef4-127">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="b9ef4-128">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="b9ef4-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ef4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ef4-129">Requirements</span></span>



| <span data-ttu-id="b9ef4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ef4-130">Requirement</span></span> | <span data-ttu-id="b9ef4-131">Value</span><span class="sxs-lookup"><span data-stu-id="b9ef4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ef4-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b9ef4-132">TAPI version</span></span><br/> | <span data-ttu-id="b9ef4-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b9ef4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b9ef4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9ef4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b9ef4-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9ef4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9ef4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="b9ef4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b9ef4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9ef4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="b9ef4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ef4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9ef4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ef4-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="b9ef4-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="b9ef4-142">**ITSdp:: get \_ Description**</span><span class="sxs-lookup"><span data-stu-id="b9ef4-142">**ITSdp::get\_Description**</span></span>](itsdp-get-description.md)
</dt> </dl>

 

