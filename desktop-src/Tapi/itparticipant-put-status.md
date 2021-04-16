---
description: El \_ método put status establece el estado de un participante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant: método de ut_Status de:p (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690388"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="8844d-103">ITParticipant::p \_ método de estado UT</span><span class="sxs-lookup"><span data-stu-id="8844d-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="8844d-104">\[**colocar \_ El estado** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8844d-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8844d-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8844d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8844d-106">El método **Put \_ status** establece el estado de un participante.</span><span class="sxs-lookup"><span data-stu-id="8844d-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="8844d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8844d-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="8844d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8844d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8844d-109">*pITStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8844d-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8844d-110">Puntero a la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="8844d-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8844d-111">*fEnable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8844d-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8844d-112">VARIANT \_ true si el participante está habilitado en la secuencia, Variant \_ false si se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="8844d-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8844d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8844d-113">Return value</span></span>

<span data-ttu-id="8844d-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8844d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8844d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8844d-115">Return code</span></span>                                                                                   | <span data-ttu-id="8844d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8844d-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8844d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8844d-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8844d-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="8844d-119"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8844d-120">Método no implementado.</span><span class="sxs-lookup"><span data-stu-id="8844d-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="8844d-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8844d-122">El parámetro *pITStream* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="8844d-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="8844d-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8844d-124">El parámetro *pITStream* no apunta a una interfaz válida.</span><span class="sxs-lookup"><span data-stu-id="8844d-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="8844d-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8844d-126">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8844d-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="8844d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8844d-127">Remarks</span></span>

<span data-ttu-id="8844d-128">Habilitar o deshabilitar el estado de un participante en un flujo permite a una aplicación silenciar esencialmente a un participante determinado.</span><span class="sxs-lookup"><span data-stu-id="8844d-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="8844d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8844d-129">Requirements</span></span>



| <span data-ttu-id="8844d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8844d-130">Requirement</span></span> | <span data-ttu-id="8844d-131">Value</span><span class="sxs-lookup"><span data-stu-id="8844d-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8844d-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8844d-132">TAPI version</span></span><br/> | <span data-ttu-id="8844d-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8844d-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="8844d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8844d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8844d-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8844d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8844d-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8844d-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8844d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8844d-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8844d-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8844d-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8844d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8844d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8844d-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="8844d-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="8844d-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="8844d-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="8844d-143">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="8844d-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

