---
description: El \_ método put SessionVersion establece la versión de la sesión.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: 'ITSdp: método de ut_SessionVersion de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690952"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="3b916-103">ITSdp::p \_ método SessionVersion UT</span><span class="sxs-lookup"><span data-stu-id="3b916-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="3b916-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3b916-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3b916-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3b916-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3b916-106">El método **Put \_ SessionVersion** establece la versión de la sesión.</span><span class="sxs-lookup"><span data-stu-id="3b916-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b916-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b916-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="3b916-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b916-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b916-109">*SessionVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b916-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b916-110">Valor de la versión de la sesión.</span><span class="sxs-lookup"><span data-stu-id="3b916-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b916-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b916-111">Return value</span></span>

<span data-ttu-id="3b916-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3b916-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3b916-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3b916-113">Return code</span></span>                                                                                   | <span data-ttu-id="3b916-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b916-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3b916-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3b916-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3b916-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3b916-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3b916-118">El parámetro *SessionVersion* no es válido.</span><span class="sxs-lookup"><span data-stu-id="3b916-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="3b916-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3b916-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3b916-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3b916-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3b916-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3b916-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3b916-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3b916-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="3b916-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3b916-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b916-125">Remarks</span></span>

<span data-ttu-id="3b916-126">El valor devuelto de este método podría ser **ULong**, pero Visual Basic no admite el tipo **ULong** .</span><span class="sxs-lookup"><span data-stu-id="3b916-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="3b916-127">Un **valor Double** es el siguiente tipo más pequeño que abarca todo el intervalo de valores requerido.</span><span class="sxs-lookup"><span data-stu-id="3b916-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="3b916-128">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="3b916-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="3b916-129">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="3b916-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b916-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b916-130">Requirements</span></span>



| <span data-ttu-id="3b916-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b916-131">Requirement</span></span> | <span data-ttu-id="3b916-132">Value</span><span class="sxs-lookup"><span data-stu-id="3b916-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b916-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3b916-133">TAPI version</span></span><br/> | <span data-ttu-id="3b916-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3b916-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3b916-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b916-135">Header</span></span><br/>       | <dl> <span data-ttu-id="3b916-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b916-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b916-137">Library</span></span><br/>      | <dl> <span data-ttu-id="3b916-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3b916-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b916-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="3b916-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b916-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b916-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b916-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b916-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="3b916-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="3b916-143">**ITSdp:: get \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="3b916-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




