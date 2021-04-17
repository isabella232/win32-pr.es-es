---
description: El método SKIP omite el siguiente número de elementos especificado en la secuencia de enumeración. Este método está oculto en Visual Basic y en los lenguajes de scripting.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'IEnumParticipant:: Skip (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690705"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="4cbfa-104">IEnumParticipant:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="4cbfa-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="4cbfa-105">\[**SKIP** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4cbfa-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4cbfa-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4cbfa-107">El método **SKIP** omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="4cbfa-108">Este método está oculto en Visual Basic y en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbfa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cbfa-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="4cbfa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cbfa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cbfa-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4cbfa-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbfa-112">Número de elementos que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cbfa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cbfa-113">Return value</span></span>

<span data-ttu-id="4cbfa-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4cbfa-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4cbfa-115">Return code</span></span>                                                                                   | <span data-ttu-id="4cbfa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cbfa-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4cbfa-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4cbfa-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4cbfa-118">El número de elementos omitidos era *Celt*.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="4cbfa-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4cbfa-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="4cbfa-120">El número de elementos omitidos no era *Celt*.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="4cbfa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4cbfa-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4cbfa-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4cbfa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cbfa-123">Requirements</span></span>



| <span data-ttu-id="4cbfa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cbfa-124">Requirement</span></span> | <span data-ttu-id="4cbfa-125">Value</span><span class="sxs-lookup"><span data-stu-id="4cbfa-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbfa-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4cbfa-126">TAPI version</span></span><br/> | <span data-ttu-id="4cbfa-127">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4cbfa-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4cbfa-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cbfa-128">Header</span></span><br/>       | <dl> <span data-ttu-id="4cbfa-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cbfa-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="4cbfa-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cbfa-130">Library</span></span><br/>      | <dl> <span data-ttu-id="4cbfa-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cbfa-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4cbfa-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4cbfa-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="4cbfa-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cbfa-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4cbfa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cbfa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cbfa-135">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="4cbfa-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="4cbfa-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="4cbfa-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




