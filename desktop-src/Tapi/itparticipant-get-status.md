---
description: El \_ método get status devuelve una variante \_ bool que indica el estado del participante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Método ITParticipant:: get_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680173"
---
# <a name="itparticipantget_status-method"></a><span data-ttu-id="c0b40-103">ITParticipant:: get \_ status (método)</span><span class="sxs-lookup"><span data-stu-id="c0b40-103">ITParticipant::get\_Status method</span></span>

<span data-ttu-id="c0b40-104">\[**obtener \_ El estado** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c0b40-104">\[**get\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c0b40-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="c0b40-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c0b40-106">El método **Get \_ status** devuelve una variante \_ bool que indica el estado del participante.</span><span class="sxs-lookup"><span data-stu-id="c0b40-106">The **get\_Status** method returns a VARIANT\_BOOL indicating participant status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b40-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0b40-107">Syntax</span></span>


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c0b40-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0b40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b40-109">*pITStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0b40-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b40-110">Puntero a la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="c0b40-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c0b40-111">*pStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c0b40-111">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b40-112">VARIANT \_ true si el participante está habilitado en la secuencia, Variant \_ false si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="c0b40-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b40-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0b40-113">Return value</span></span>

<span data-ttu-id="c0b40-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c0b40-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c0b40-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c0b40-115">Return code</span></span>                                                                                   | <span data-ttu-id="c0b40-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0b40-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0b40-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c0b40-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c0b40-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="c0b40-119"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c0b40-120">Método no implementado.</span><span class="sxs-lookup"><span data-stu-id="c0b40-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c0b40-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c0b40-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c0b40-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="c0b40-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c0b40-124">El parámetro *pITStream* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="c0b40-124">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="c0b40-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c0b40-126">El parámetro *pITStream* no apunta a una interfaz válida.</span><span class="sxs-lookup"><span data-stu-id="c0b40-126">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0b40-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0b40-127">Remarks</span></span>

<span data-ttu-id="c0b40-128">Habilitar o deshabilitar el estado de un participante en un flujo permite a una aplicación silenciar esencialmente a un participante determinado.</span><span class="sxs-lookup"><span data-stu-id="c0b40-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b40-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0b40-129">Requirements</span></span>



| <span data-ttu-id="c0b40-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0b40-130">Requirement</span></span> | <span data-ttu-id="c0b40-131">Value</span><span class="sxs-lookup"><span data-stu-id="c0b40-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b40-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c0b40-132">TAPI version</span></span><br/> | <span data-ttu-id="c0b40-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c0b40-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="c0b40-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0b40-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c0b40-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0b40-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0b40-136">Library</span></span><br/>      | <dl> <span data-ttu-id="c0b40-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="c0b40-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0b40-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="c0b40-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b40-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b40-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0b40-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b40-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c0b40-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="c0b40-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="c0b40-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="c0b40-143">**Estado de put \_**</span><span class="sxs-lookup"><span data-stu-id="c0b40-143">**put\_Status**</span></span>](itparticipant-put-status.md)
</dt> </dl>

 

