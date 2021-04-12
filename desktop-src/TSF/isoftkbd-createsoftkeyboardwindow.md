---
title: Método ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: El método ISoftKbd CreateSoftKeyboardWindow crea una ventana de teclado en pantalla.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Método CreateSoftKeyboardWindow marco de trabajo de servicios de texto
- Método CreateSoftKeyboardWindow marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534792"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="54363-106">ISoftKbd:: CreateSoftKeyboardWindow (método)</span><span class="sxs-lookup"><span data-stu-id="54363-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="54363-107">El método **ISoftKbd:: CreateSoftKeyboardWindow** crea una ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="54363-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54363-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="54363-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54363-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54363-110">*hOwner* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54363-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54363-111">Identificador de la ventana que va a contener el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="54363-112">*\_ Tipo de TitleBar* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="54363-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54363-113">Tipo de barra de título de la ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="54363-114">Los tipos posibles se definen mediante la enumeración de [**\_ tipo TITLEBAR**](titlebar-type.md) .</span><span class="sxs-lookup"><span data-stu-id="54363-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="54363-115">*xPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54363-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54363-116">Posición x de la esquina superior izquierda de la ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="54363-117">*yPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54363-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54363-118">Posición y de la esquina superior izquierda de la ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="54363-119">*ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="54363-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54363-120">Ancho de la ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="54363-121">*alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="54363-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54363-122">Alto de la ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="54363-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54363-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54363-123">Return value</span></span>

<span data-ttu-id="54363-124">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="54363-124">This method can return one of these values.</span></span>



| <span data-ttu-id="54363-125">Value</span><span class="sxs-lookup"><span data-stu-id="54363-125">Value</span></span>                                                                                        | <span data-ttu-id="54363-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="54363-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="54363-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="54363-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="54363-128">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="54363-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="54363-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="54363-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="54363-130">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="54363-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="54363-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54363-131">Requirements</span></span>



| <span data-ttu-id="54363-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="54363-132">Requirement</span></span> | <span data-ttu-id="54363-133">Value</span><span class="sxs-lookup"><span data-stu-id="54363-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54363-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54363-134">Minimum supported client</span></span><br/> | <span data-ttu-id="54363-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="54363-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="54363-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54363-136">Minimum supported server</span></span><br/> | <span data-ttu-id="54363-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54363-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54363-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="54363-138">Redistributable</span></span><br/>          | <span data-ttu-id="54363-139">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="54363-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="54363-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54363-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="54363-141"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="54363-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="54363-142">IDL</span><span class="sxs-lookup"><span data-stu-id="54363-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54363-143"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54363-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="54363-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54363-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54363-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54363-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54363-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="54363-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54363-147">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="54363-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="54363-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="54363-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="54363-149">**ISoftKbd::D estroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="54363-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="54363-150">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="54363-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="54363-151">**tipo de TITLEBAR \_**</span><span class="sxs-lookup"><span data-stu-id="54363-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





