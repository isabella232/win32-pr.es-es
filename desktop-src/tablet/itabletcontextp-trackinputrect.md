---
description: Actualiza el digitalizador de Tablet PC a las coordenadas de asignación de ubicación de la ventana.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'ITabletContextP:: TrackInputRect (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716905"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="26ac1-103">ITabletContextP:: TrackInputRect (método)</span><span class="sxs-lookup"><span data-stu-id="26ac1-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="26ac1-104">Actualiza el digitalizador de Tablet PC a las coordenadas de asignación de ubicación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="26ac1-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ac1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26ac1-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="26ac1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ac1-107">*prcInput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="26ac1-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26ac1-108">El nuevo rectángulo de la ventana de entrada después de actualizar la asignación entre las coordenadas de ventana y digitalizador.</span><span class="sxs-lookup"><span data-stu-id="26ac1-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ac1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26ac1-109">Return value</span></span>

<span data-ttu-id="26ac1-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="26ac1-110">This method can return one of these values.</span></span>



| <span data-ttu-id="26ac1-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="26ac1-111">Return code</span></span>                                                                            | <span data-ttu-id="26ac1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="26ac1-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="26ac1-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="26ac1-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="26ac1-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="26ac1-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="26ac1-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="26ac1-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="26ac1-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="26ac1-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26ac1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26ac1-117">Remarks</span></span>

<span data-ttu-id="26ac1-118">Llame a este método siempre que cambie la ubicación de la ventana en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="26ac1-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ac1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26ac1-119">Requirements</span></span>



| <span data-ttu-id="26ac1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26ac1-120">Requirement</span></span> | <span data-ttu-id="26ac1-121">Value</span><span class="sxs-lookup"><span data-stu-id="26ac1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26ac1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26ac1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26ac1-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="26ac1-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="26ac1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26ac1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26ac1-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="26ac1-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="26ac1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26ac1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="26ac1-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26ac1-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ac1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="26ac1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ac1-129">**Interfaz ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="26ac1-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




