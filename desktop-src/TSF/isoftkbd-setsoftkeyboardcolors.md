---
title: Método ISoftKbd SetSoftKeyboardColors (Softkbdc. h)
description: El método ISoftKbd SetSoftKeyboardColors establece el color del teclado en pantalla para el tipo de color especificado.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Método SetSoftKeyboardColors marco de trabajo de servicios de texto
- Método SetSoftKeyboardColors marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "105689600"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="03f25-106">ISoftKbd:: SetSoftKeyboardColors (método)</span><span class="sxs-lookup"><span data-stu-id="03f25-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="03f25-107">El método **ISoftKbd:: SetSoftKeyboardColors** establece el color del teclado en pantalla para el tipo de color especificado.</span><span class="sxs-lookup"><span data-stu-id="03f25-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03f25-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="03f25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03f25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f25-110">*colorType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03f25-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03f25-111">Valor que especifica el tipo de color del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="03f25-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="03f25-112">Se definen los valores posibles para la enumeración [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="03f25-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="03f25-113">*Color* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="03f25-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03f25-114">Un valor [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits que especifica un color RGB.</span><span class="sxs-lookup"><span data-stu-id="03f25-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f25-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03f25-115">Return value</span></span>

<span data-ttu-id="03f25-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="03f25-116">This method can return one of these values.</span></span>



| <span data-ttu-id="03f25-117">Value</span><span class="sxs-lookup"><span data-stu-id="03f25-117">Value</span></span>                                                                                        | <span data-ttu-id="03f25-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="03f25-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="03f25-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="03f25-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="03f25-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="03f25-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="03f25-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="03f25-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="03f25-122">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="03f25-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="03f25-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03f25-123">Requirements</span></span>



| <span data-ttu-id="03f25-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f25-124">Requirement</span></span> | <span data-ttu-id="03f25-125">Value</span><span class="sxs-lookup"><span data-stu-id="03f25-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f25-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03f25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="03f25-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="03f25-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="03f25-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03f25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="03f25-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03f25-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03f25-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="03f25-130">Redistributable</span></span><br/>          | <span data-ttu-id="03f25-131">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="03f25-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="03f25-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03f25-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f25-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="03f25-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="03f25-134">IDL</span><span class="sxs-lookup"><span data-stu-id="03f25-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03f25-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03f25-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="03f25-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03f25-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f25-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f25-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f25-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="03f25-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f25-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="03f25-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="03f25-140">**ISoftKbd::GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="03f25-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="03f25-141">**Property**</span><span class="sxs-lookup"><span data-stu-id="03f25-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="03f25-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="03f25-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

