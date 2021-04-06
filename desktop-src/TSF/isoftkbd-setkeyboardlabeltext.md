---
title: Método ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: El método ISoftKbd SetKeyboardLabelText establece el texto de la etiqueta del diseño de un teclado en pantalla.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Método SetKeyboardLabelText marco de trabajo de servicios de texto
- Método SetKeyboardLabelText marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803242"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="7ed96-106">ISoftKbd:: SetKeyboardLabelText (método)</span><span class="sxs-lookup"><span data-stu-id="7ed96-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="7ed96-107">El método **ISoftKbd:: SetKeyboardLabelText** establece el texto de la etiqueta del diseño de un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="7ed96-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed96-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ed96-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="7ed96-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ed96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed96-110">*hKl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7ed96-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed96-111">Identificador que se usa para recuperar el diseño instalado para el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="7ed96-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ed96-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ed96-112">Return value</span></span>

<span data-ttu-id="7ed96-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7ed96-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7ed96-114">Value</span><span class="sxs-lookup"><span data-stu-id="7ed96-114">Value</span></span>                                                                                        | <span data-ttu-id="7ed96-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ed96-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="7ed96-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7ed96-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7ed96-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ed96-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="7ed96-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ed96-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7ed96-119">El parámetro *hKl* no es válido.</span><span class="sxs-lookup"><span data-stu-id="7ed96-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ed96-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ed96-120">Requirements</span></span>



| <span data-ttu-id="7ed96-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed96-121">Requirement</span></span> | <span data-ttu-id="7ed96-122">Value</span><span class="sxs-lookup"><span data-stu-id="7ed96-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed96-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ed96-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed96-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7ed96-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7ed96-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ed96-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed96-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ed96-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7ed96-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7ed96-127">Redistributable</span></span><br/>          | <span data-ttu-id="7ed96-128">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7ed96-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="7ed96-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ed96-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed96-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed96-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="7ed96-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7ed96-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ed96-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ed96-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ed96-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ed96-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ed96-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ed96-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ed96-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ed96-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed96-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="7ed96-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="7ed96-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="7ed96-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





