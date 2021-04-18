---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual. Este método está oculto en Visual Basic y en los lenguajes de scripting.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'IEnumParticipant:: Clone (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681141"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="b526d-104">IEnumParticipant:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="b526d-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="b526d-105">\[**Clone** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b526d-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b526d-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b526d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b526d-107">El método **Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="b526d-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="b526d-108">Este método está oculto en Visual Basic y en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="b526d-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b526d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b526d-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="b526d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b526d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b526d-111">*ppEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b526d-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b526d-112">Puntero a la nueva interfaz [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="b526d-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b526d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b526d-113">Return value</span></span>

<span data-ttu-id="b526d-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b526d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b526d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b526d-115">Return code</span></span>                                                                                   | <span data-ttu-id="b526d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b526d-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b526d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b526d-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b526d-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b526d-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b526d-120">El parámetro *ppEnum* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="b526d-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="b526d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b526d-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b526d-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b526d-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="b526d-124">Error por razones desconocidas.</span><span class="sxs-lookup"><span data-stu-id="b526d-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="b526d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b526d-125">Remarks</span></span>

<span data-ttu-id="b526d-126">TAPI llama al método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la interfaz [**IEnumParticipant**](ienumparticipant.md) devuelta por **IEnumParticipant:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="b526d-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="b526d-127">La aplicación debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la interfaz **IEnumParticipant** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="b526d-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b526d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b526d-128">Requirements</span></span>



| <span data-ttu-id="b526d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b526d-129">Requirement</span></span> | <span data-ttu-id="b526d-130">Value</span><span class="sxs-lookup"><span data-stu-id="b526d-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b526d-131">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b526d-131">TAPI version</span></span><br/> | <span data-ttu-id="b526d-132">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b526d-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b526d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b526d-133">Header</span></span><br/>       | <dl> <span data-ttu-id="b526d-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="b526d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b526d-135">Library</span></span><br/>      | <dl> <span data-ttu-id="b526d-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b526d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b526d-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="b526d-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b526d-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b526d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b526d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b526d-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="b526d-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="b526d-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="b526d-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

