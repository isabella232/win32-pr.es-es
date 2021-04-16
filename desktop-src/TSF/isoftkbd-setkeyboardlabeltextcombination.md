---
title: Método ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: El método ISoftKbd SetKeyboardLabelTextCombination establece una combinación de etiqueta y texto que se usa para describir un teclado en pantalla.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Método SetKeyboardLabelTextCombination marco de trabajo de servicios de texto
- Método SetKeyboardLabelTextCombination marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686113"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="60cf0-106">ISoftKbd:: SetKeyboardLabelTextCombination (método)</span><span class="sxs-lookup"><span data-stu-id="60cf0-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="60cf0-107">El método **ISoftKbd:: SetKeyboardLabelTextCombination** establece una combinación de etiqueta y texto que se usa para describir un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="60cf0-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cf0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60cf0-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="60cf0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60cf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60cf0-110">*nModifierCombination* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60cf0-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cf0-111">Combinación de etiqueta y texto que se usa para describir el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="60cf0-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60cf0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60cf0-112">Return value</span></span>

<span data-ttu-id="60cf0-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="60cf0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="60cf0-114">Value</span><span class="sxs-lookup"><span data-stu-id="60cf0-114">Value</span></span>                                                                                        | <span data-ttu-id="60cf0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="60cf0-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="60cf0-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="60cf0-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="60cf0-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="60cf0-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="60cf0-119">El parámetro *nModifierCombination* no es válido.</span><span class="sxs-lookup"><span data-stu-id="60cf0-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60cf0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60cf0-120">Requirements</span></span>



| <span data-ttu-id="60cf0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="60cf0-121">Requirement</span></span> | <span data-ttu-id="60cf0-122">Value</span><span class="sxs-lookup"><span data-stu-id="60cf0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60cf0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60cf0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="60cf0-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="60cf0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="60cf0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60cf0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="60cf0-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60cf0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="60cf0-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="60cf0-127">Redistributable</span></span><br/>          | <span data-ttu-id="60cf0-128">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="60cf0-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="60cf0-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60cf0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60cf0-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="60cf0-131">IDL</span><span class="sxs-lookup"><span data-stu-id="60cf0-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60cf0-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="60cf0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60cf0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60cf0-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60cf0-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60cf0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="60cf0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cf0-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="60cf0-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="60cf0-137">**ISoftKbd::SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="60cf0-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





