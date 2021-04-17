---
title: Método ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: El método ISoftKbd AdviseSoftKeyboardEventSink instala un receptor de eventos de teclado en pantalla para controlar las notificaciones de OnKeySelection desde el teclado en pantalla.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Método AdviseSoftKeyboardEventSink marco de trabajo de servicios de texto
- Método AdviseSoftKeyboardEventSink marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422508"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="6c929-106">ISoftKbd:: AdviseSoftKeyboardEventSink (método)</span><span class="sxs-lookup"><span data-stu-id="6c929-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="6c929-107">El método **ISoftKbd:: AdviseSoftKeyboardEventSink** instala un receptor de eventos de teclado en pantalla para controlar las notificaciones de OnKeySelection desde el teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="6c929-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c929-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c929-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="6c929-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c929-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c929-110">*dwKeyboardId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c929-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c929-111">Identificador del teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="6c929-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="6c929-112">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c929-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c929-113">Identificador de interfaz para la interfaz de receptor.</span><span class="sxs-lookup"><span data-stu-id="6c929-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="6c929-114">*punk* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c929-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c929-115">Puntero a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para la interfaz de receptor especificada por *riid*.</span><span class="sxs-lookup"><span data-stu-id="6c929-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="6c929-116">Este parámetro no se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="6c929-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c929-117">*pdwCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c929-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c929-118">Puntero al búfer en el que este método recupera la "cookie" de teclado blando utilizada para la conexión al cliente.</span><span class="sxs-lookup"><span data-stu-id="6c929-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="6c929-119">La cookie debe ser única para cada conexión.</span><span class="sxs-lookup"><span data-stu-id="6c929-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c929-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c929-120">Return value</span></span>

<span data-ttu-id="6c929-121">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6c929-121">This method can return one of these values.</span></span>



| <span data-ttu-id="6c929-122">Value</span><span class="sxs-lookup"><span data-stu-id="6c929-122">Value</span></span>                                                                                        | <span data-ttu-id="6c929-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c929-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6c929-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6c929-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6c929-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c929-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="6c929-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6c929-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6c929-127">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="6c929-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c929-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c929-128">Requirements</span></span>



| <span data-ttu-id="6c929-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c929-129">Requirement</span></span> | <span data-ttu-id="6c929-130">Value</span><span class="sxs-lookup"><span data-stu-id="6c929-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c929-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c929-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6c929-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c929-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c929-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c929-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6c929-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c929-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6c929-135">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6c929-135">Redistributable</span></span><br/>          | <span data-ttu-id="6c929-136">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c929-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="6c929-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c929-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c929-138"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c929-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="6c929-139">IDL</span><span class="sxs-lookup"><span data-stu-id="6c929-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c929-140"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c929-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="6c929-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c929-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c929-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c929-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c929-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c929-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c929-144">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="6c929-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="6c929-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="6c929-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

