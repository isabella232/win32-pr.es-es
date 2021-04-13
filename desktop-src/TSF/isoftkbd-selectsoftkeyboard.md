---
title: Método ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: El método ISoftKbd SelectSoftKeyboard selecciona el teclado en pantalla especificado.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Método SelectSoftKeyboard marco de trabajo de servicios de texto
- Método SelectSoftKeyboard marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534900"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="41a5f-106">ISoftKbd:: SelectSoftKeyboard (método)</span><span class="sxs-lookup"><span data-stu-id="41a5f-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="41a5f-107">El método **ISoftKbd:: SelectSoftKeyboard** selecciona el teclado en pantalla especificado.</span><span class="sxs-lookup"><span data-stu-id="41a5f-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a5f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41a5f-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="41a5f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41a5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a5f-110">*dwKeyboardId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41a5f-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a5f-111">Identificador del teclado en pantalla que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="41a5f-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a5f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41a5f-112">Return value</span></span>

<span data-ttu-id="41a5f-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="41a5f-113">This method can return one of these values.</span></span>



| <span data-ttu-id="41a5f-114">Value</span><span class="sxs-lookup"><span data-stu-id="41a5f-114">Value</span></span>                                                                                        | <span data-ttu-id="41a5f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="41a5f-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="41a5f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="41a5f-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="41a5f-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="41a5f-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="41a5f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="41a5f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="41a5f-119">El parámetro *dwKeyboardId* no es válido.</span><span class="sxs-lookup"><span data-stu-id="41a5f-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="41a5f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41a5f-120">Requirements</span></span>



| <span data-ttu-id="41a5f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41a5f-121">Requirement</span></span> | <span data-ttu-id="41a5f-122">Value</span><span class="sxs-lookup"><span data-stu-id="41a5f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41a5f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41a5f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41a5f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41a5f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="41a5f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41a5f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41a5f-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41a5f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="41a5f-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="41a5f-127">Redistributable</span></span><br/>          | <span data-ttu-id="41a5f-128">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41a5f-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="41a5f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41a5f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a5f-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a5f-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="41a5f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="41a5f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41a5f-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41a5f-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="41a5f-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41a5f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41a5f-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41a5f-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41a5f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="41a5f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a5f-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="41a5f-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





