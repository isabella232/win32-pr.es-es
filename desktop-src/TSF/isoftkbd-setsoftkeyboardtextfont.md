---
title: Método ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: El método ISoftKbd SetSoftKeyboardTextFont establece la fuente de texto utilizada por un teclado en pantalla.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Método SetSoftKeyboardTextFont marco de trabajo de servicios de texto
- Método SetSoftKeyboardTextFont marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686112"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="0161b-106">ISoftKbd:: SetSoftKeyboardTextFont (método)</span><span class="sxs-lookup"><span data-stu-id="0161b-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="0161b-107">El método **ISoftKbd:: SetSoftKeyboardTextFont** establece la fuente de texto utilizada por un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0161b-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="0161b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0161b-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="0161b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0161b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0161b-110">*pLogFont* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0161b-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0161b-111">Puntero a una estructura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define la fuente del texto para el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="0161b-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0161b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0161b-112">Return value</span></span>

<span data-ttu-id="0161b-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0161b-113">This method can return one of these values.</span></span>



| <span data-ttu-id="0161b-114">Value</span><span class="sxs-lookup"><span data-stu-id="0161b-114">Value</span></span>                                                                                        | <span data-ttu-id="0161b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0161b-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="0161b-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0161b-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0161b-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0161b-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="0161b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0161b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0161b-119">El parámetro *pLogFont* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0161b-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0161b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0161b-120">Requirements</span></span>



| <span data-ttu-id="0161b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0161b-121">Requirement</span></span> | <span data-ttu-id="0161b-122">Value</span><span class="sxs-lookup"><span data-stu-id="0161b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0161b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0161b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0161b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0161b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0161b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0161b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0161b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0161b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0161b-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0161b-127">Redistributable</span></span><br/>          | <span data-ttu-id="0161b-128">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0161b-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="0161b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0161b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0161b-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0161b-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="0161b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="0161b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0161b-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0161b-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="0161b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0161b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0161b-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0161b-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0161b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0161b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0161b-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="0161b-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="0161b-137">**ISoftKbd::GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="0161b-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

