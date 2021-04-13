---
title: Método ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: El método ISoftKbd SetSoftKeyboardPosSize establece la posición inicial y el tamaño de un teclado en pantalla.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Método SetSoftKeyboardPosSize marco de trabajo de servicios de texto
- Método SetSoftKeyboardPosSize marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492100"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a><span data-ttu-id="0852c-106">ISoftKbd:: SetSoftKeyboardPosSize (método)</span><span class="sxs-lookup"><span data-stu-id="0852c-106">ISoftKbd::SetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="0852c-107">El método **ISoftKbd:: SetSoftKeyboardPosSize** establece la posición inicial y el tamaño de un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0852c-107">The **ISoftKbd::SetSoftKeyboardPosSize** method sets the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="0852c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0852c-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a><span data-ttu-id="0852c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0852c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0852c-110">*StartPoint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0852c-110">*StartPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0852c-111">Una estructura de [punto](/previous-versions//dd162805(v=vs.85)) que indica las coordenadas de la posición superior izquierda del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0852c-111">A [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="0852c-112">*ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0852c-112">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0852c-113">Ancho del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0852c-113">Width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="0852c-114">*alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0852c-114">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0852c-115">Alto del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0852c-115">Height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0852c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0852c-116">Return value</span></span>

<span data-ttu-id="0852c-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0852c-117">This method can return one of these values.</span></span>



| <span data-ttu-id="0852c-118">Value</span><span class="sxs-lookup"><span data-stu-id="0852c-118">Value</span></span>                                                                                        | <span data-ttu-id="0852c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0852c-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0852c-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0852c-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0852c-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0852c-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="0852c-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0852c-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0852c-123">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="0852c-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0852c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0852c-124">Requirements</span></span>



| <span data-ttu-id="0852c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0852c-125">Requirement</span></span> | <span data-ttu-id="0852c-126">Value</span><span class="sxs-lookup"><span data-stu-id="0852c-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0852c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0852c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0852c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0852c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0852c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0852c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0852c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0852c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0852c-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0852c-131">Redistributable</span></span><br/>          | <span data-ttu-id="0852c-132">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0852c-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="0852c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0852c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0852c-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0852c-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="0852c-135">IDL</span><span class="sxs-lookup"><span data-stu-id="0852c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0852c-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0852c-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="0852c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0852c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0852c-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0852c-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0852c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0852c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0852c-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="0852c-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

