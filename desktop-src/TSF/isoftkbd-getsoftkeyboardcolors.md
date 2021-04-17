---
title: Método ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardColors recupera el color del teclado blando correspondiente al tipo de color proporcionado.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Método GetSoftKeyboardColors marco de trabajo de servicios de texto
- Método GetSoftKeyboardColors marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "105689598"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="04ac9-106">ISoftKbd:: GetSoftKeyboardColors (método)</span><span class="sxs-lookup"><span data-stu-id="04ac9-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="04ac9-107">El método **ISoftKbd:: GetSoftKeyboardColors** recupera el color del teclado blando correspondiente al tipo de color proporcionado.</span><span class="sxs-lookup"><span data-stu-id="04ac9-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ac9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04ac9-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="04ac9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04ac9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ac9-110">*colorType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04ac9-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ac9-111">Valor que especifica el tipo de color que se va a recuperar para el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="04ac9-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="04ac9-112">Se definen los valores posibles para la enumeración [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="04ac9-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="04ac9-113">*lpColor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="04ac9-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04ac9-114">Puntero a un búfer en el que este método recupera un valor [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits que especifica un color RGB.</span><span class="sxs-lookup"><span data-stu-id="04ac9-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ac9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04ac9-115">Return value</span></span>

<span data-ttu-id="04ac9-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="04ac9-116">This method can return one of these values.</span></span>



| <span data-ttu-id="04ac9-117">Value</span><span class="sxs-lookup"><span data-stu-id="04ac9-117">Value</span></span>                                                                                        | <span data-ttu-id="04ac9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="04ac9-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="04ac9-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="04ac9-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="04ac9-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="04ac9-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="04ac9-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="04ac9-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="04ac9-122">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="04ac9-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="04ac9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ac9-123">Requirements</span></span>



| <span data-ttu-id="04ac9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ac9-124">Requirement</span></span> | <span data-ttu-id="04ac9-125">Value</span><span class="sxs-lookup"><span data-stu-id="04ac9-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04ac9-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ac9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04ac9-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04ac9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="04ac9-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ac9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04ac9-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04ac9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04ac9-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="04ac9-130">Redistributable</span></span><br/>          | <span data-ttu-id="04ac9-131">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04ac9-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="04ac9-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04ac9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ac9-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ac9-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="04ac9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="04ac9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04ac9-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04ac9-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="04ac9-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04ac9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ac9-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ac9-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ac9-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="04ac9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ac9-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="04ac9-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="04ac9-140">**ISoftKbd::SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="04ac9-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="04ac9-141">**Property**</span><span class="sxs-lookup"><span data-stu-id="04ac9-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="04ac9-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="04ac9-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

