---
title: Método ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardTextFont recupera la fuente de texto utilizada por un teclado en pantalla.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Método GetSoftKeyboardTextFont marco de trabajo de servicios de texto
- Método GetSoftKeyboardTextFont marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150809"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="1c837-106">ISoftKbd:: GetSoftKeyboardTextFont (método)</span><span class="sxs-lookup"><span data-stu-id="1c837-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="1c837-107">El método **ISoftKbd:: GetSoftKeyboardTextFont** recupera la fuente de texto utilizada por un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="1c837-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c837-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c837-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="1c837-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c837-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c837-110">*pLogFont* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c837-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c837-111">Puntero a un búfer en el que este método recupera una estructura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define la fuente del texto para el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="1c837-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c837-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c837-112">Return value</span></span>

<span data-ttu-id="1c837-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1c837-113">This method can return one of these values.</span></span>



| <span data-ttu-id="1c837-114">Value</span><span class="sxs-lookup"><span data-stu-id="1c837-114">Value</span></span>                                                                                        | <span data-ttu-id="1c837-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c837-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1c837-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1c837-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1c837-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c837-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="1c837-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1c837-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1c837-119">El parámetro *pLogFont* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1c837-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c837-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c837-120">Requirements</span></span>



| <span data-ttu-id="1c837-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c837-121">Requirement</span></span> | <span data-ttu-id="1c837-122">Value</span><span class="sxs-lookup"><span data-stu-id="1c837-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c837-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c837-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1c837-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1c837-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1c837-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c837-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1c837-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1c837-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1c837-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1c837-127">Redistributable</span></span><br/>          | <span data-ttu-id="1c837-128">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1c837-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1c837-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c837-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c837-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c837-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1c837-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1c837-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c837-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c837-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="1c837-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c837-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c837-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c837-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c837-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c837-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c837-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="1c837-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="1c837-137">**ISoftKbd::SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="1c837-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

