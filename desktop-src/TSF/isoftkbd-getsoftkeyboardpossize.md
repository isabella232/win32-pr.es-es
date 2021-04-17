---
title: Método ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardPosSize recupera la posición inicial y el tamaño de un teclado en pantalla.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Método GetSoftKeyboardPosSize marco de trabajo de servicios de texto
- Método GetSoftKeyboardPosSize marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359780"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="f51ed-106">ISoftKbd:: GetSoftKeyboardPosSize (método)</span><span class="sxs-lookup"><span data-stu-id="f51ed-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="f51ed-107">El método **ISoftKbd:: GetSoftKeyboardPosSize** recupera la posición inicial y el tamaño de un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="f51ed-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f51ed-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="f51ed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f51ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f51ed-110">*lpStartPoint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f51ed-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51ed-111">Puntero a un búfer en el que este método recupera una estructura de [punto](/previous-versions//dd162805(v=vs.85)) que indica las coordenadas de la posición superior izquierda del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="f51ed-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="f51ed-112">*lpwidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f51ed-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51ed-113">Puntero a un búfer en el que este método recupera el ancho del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="f51ed-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="f51ed-114">*lpheight* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f51ed-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51ed-115">Puntero a un búfer en el que este método recupera el alto del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="f51ed-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f51ed-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f51ed-116">Return value</span></span>

<span data-ttu-id="f51ed-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f51ed-117">This method can return one of these values.</span></span>



| <span data-ttu-id="f51ed-118">Value</span><span class="sxs-lookup"><span data-stu-id="f51ed-118">Value</span></span>                                                                                        | <span data-ttu-id="f51ed-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f51ed-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f51ed-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f51ed-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f51ed-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f51ed-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="f51ed-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f51ed-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f51ed-123">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="f51ed-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f51ed-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51ed-124">Requirements</span></span>



| <span data-ttu-id="f51ed-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51ed-125">Requirement</span></span> | <span data-ttu-id="f51ed-126">Value</span><span class="sxs-lookup"><span data-stu-id="f51ed-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f51ed-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f51ed-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f51ed-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f51ed-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f51ed-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f51ed-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f51ed-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f51ed-131">Redistributable</span></span><br/>          | <span data-ttu-id="f51ed-132">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f51ed-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f51ed-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f51ed-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f51ed-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f51ed-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f51ed-135">IDL</span><span class="sxs-lookup"><span data-stu-id="f51ed-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f51ed-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f51ed-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f51ed-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f51ed-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f51ed-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f51ed-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f51ed-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f51ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51ed-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f51ed-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="f51ed-141">**ISoftKbd::SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="f51ed-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

