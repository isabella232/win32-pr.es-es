---
title: Método ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: El método ISoftKbd DestroySoftKeyboardWindow destruye una ventana de teclado en pantalla.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Método DestroySoftKeyboardWindow marco de trabajo de servicios de texto
- Método DestroySoftKeyboardWindow marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685991"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="f10e7-106">ISoftKbd::D método estroySoftKeyboardWindow</span><span class="sxs-lookup"><span data-stu-id="f10e7-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="f10e7-107">El método **ISoftKbd::D estroysoftkeyboardwindow** destruye una ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="f10e7-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f10e7-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="f10e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f10e7-109">Parameters</span></span>

<span data-ttu-id="f10e7-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f10e7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f10e7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f10e7-111">Return value</span></span>

<span data-ttu-id="f10e7-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f10e7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f10e7-113">Value</span><span class="sxs-lookup"><span data-stu-id="f10e7-113">Value</span></span>                                                                                | <span data-ttu-id="f10e7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f10e7-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f10e7-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f10e7-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f10e7-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f10e7-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f10e7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f10e7-117">Remarks</span></span>

<span data-ttu-id="f10e7-118">Este método quita una ventana de teclado en pantalla creada previamente con una llamada a [**ISoftKbd:: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span><span class="sxs-lookup"><span data-stu-id="f10e7-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f10e7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f10e7-119">Requirements</span></span>



| <span data-ttu-id="f10e7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f10e7-120">Requirement</span></span> | <span data-ttu-id="f10e7-121">Value</span><span class="sxs-lookup"><span data-stu-id="f10e7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f10e7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f10e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f10e7-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f10e7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f10e7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f10e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f10e7-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f10e7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f10e7-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f10e7-126">Redistributable</span></span><br/>          | <span data-ttu-id="f10e7-127">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f10e7-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f10e7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f10e7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f10e7-129"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f10e7-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f10e7-130">IDL</span><span class="sxs-lookup"><span data-stu-id="f10e7-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f10e7-131"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f10e7-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f10e7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f10e7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f10e7-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f10e7-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f10e7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f10e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f10e7-135">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f10e7-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="f10e7-136">**ISoftKbd::CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="f10e7-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





