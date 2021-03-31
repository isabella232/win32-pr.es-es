---
description: Devuelve un valor que representa las funciones del hardware de Tablet PC.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'ITablet:: GetHardwareCaps (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912341"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="204e0-103">ITablet:: GetHardwareCaps (método)</span><span class="sxs-lookup"><span data-stu-id="204e0-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="204e0-104">Devuelve un valor que representa las funciones del hardware de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="204e0-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="204e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="204e0-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="204e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="204e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="204e0-107">*pdwCaps* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="204e0-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="204e0-108">Marcas de bits que representan las capacidades del hardware de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="204e0-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="204e0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="204e0-109">Return value</span></span>

<span data-ttu-id="204e0-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="204e0-110">This method can return one of these values.</span></span>



| <span data-ttu-id="204e0-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="204e0-111">Return code</span></span>                                                                            | <span data-ttu-id="204e0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="204e0-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="204e0-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="204e0-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="204e0-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="204e0-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="204e0-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="204e0-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="204e0-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="204e0-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="204e0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="204e0-117">Remarks</span></span>

<span data-ttu-id="204e0-118">El parámetro *pdwCaps* es un conjunto de marcadores de bits que describen las capacidades de hardware de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="204e0-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="204e0-119">En la tabla siguiente se describen estas marcas.</span><span class="sxs-lookup"><span data-stu-id="204e0-119">The following table describes these flags.</span></span>



| <span data-ttu-id="204e0-120">Nombre de marca</span><span class="sxs-lookup"><span data-stu-id="204e0-120">Flag Name</span></span>                         | <span data-ttu-id="204e0-121">Value</span><span class="sxs-lookup"><span data-stu-id="204e0-121">Value</span></span>                 | <span data-ttu-id="204e0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="204e0-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="204e0-123">THWC \_ integrado</span><span class="sxs-lookup"><span data-stu-id="204e0-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="204e0-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="204e0-124">0x00000001</span></span><br/> | <span data-ttu-id="204e0-125">Indica que la pantalla y el digitalizador comparten la misma superficie.</span><span class="sxs-lookup"><span data-stu-id="204e0-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="204e0-126">THWC \_ CSR \_ debe \_ tocar</span><span class="sxs-lookup"><span data-stu-id="204e0-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="204e0-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="204e0-127">0x00000002</span></span><br/> | <span data-ttu-id="204e0-128">Indica que el cursor debe estar en contacto físico con el dispositivo para informar de la posición.</span><span class="sxs-lookup"><span data-stu-id="204e0-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="204e0-129">\_proximidad THWC \_</span><span class="sxs-lookup"><span data-stu-id="204e0-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="204e0-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="204e0-130">0x00000004</span></span><br/> | <span data-ttu-id="204e0-131">Indica que el dispositivo puede generar eventos cuando el cursor entra y sale del intervalo de detección física.</span><span class="sxs-lookup"><span data-stu-id="204e0-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="204e0-132">CSR de THWC \_ PHYSID \_</span><span class="sxs-lookup"><span data-stu-id="204e0-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="204e0-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="204e0-133">0x00000008</span></span><br/> | <span data-ttu-id="204e0-134">Indica que el dispositivo puede identificar de forma única el cursor activo en el hardware.</span><span class="sxs-lookup"><span data-stu-id="204e0-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="204e0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="204e0-135">Requirements</span></span>



| <span data-ttu-id="204e0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="204e0-136">Requirement</span></span> | <span data-ttu-id="204e0-137">Value</span><span class="sxs-lookup"><span data-stu-id="204e0-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="204e0-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="204e0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="204e0-139">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="204e0-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="204e0-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="204e0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="204e0-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="204e0-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="204e0-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="204e0-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="204e0-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="204e0-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="204e0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="204e0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204e0-145">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="204e0-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




