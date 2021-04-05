---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: El método ISoftKbd UnadviseSoftKeyboardEventSink quita un receptor de eventos de teclado en pantalla.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Método UnadviseSoftKeyboardEventSink marco de trabajo de servicios de texto
- Método UnadviseSoftKeyboardEventSink marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803241"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="84a30-106">ISoftKbd:: UnadviseSoftKeyboardEventSink (método)</span><span class="sxs-lookup"><span data-stu-id="84a30-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="84a30-107">El método **ISoftKbd:: UnadviseSoftKeyboardEventSink** quita un receptor de eventos de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="84a30-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a30-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84a30-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="84a30-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84a30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a30-110">*TID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84a30-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84a30-111">Identificador del cliente que posee el receptor de eventos de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="84a30-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="84a30-112">Este valor se pasó cuando se instaló el receptor de eventos mediante [ISoftKbd:: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span><span class="sxs-lookup"><span data-stu-id="84a30-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a30-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84a30-113">Return value</span></span>

<span data-ttu-id="84a30-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="84a30-114">This method can return one of these values.</span></span>



| <span data-ttu-id="84a30-115">Value</span><span class="sxs-lookup"><span data-stu-id="84a30-115">Value</span></span>                                                                                                   | <span data-ttu-id="84a30-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="84a30-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="84a30-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="84a30-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="84a30-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="84a30-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="84a30-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="84a30-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="84a30-120">El parámetro *TID* no es válido.</span><span class="sxs-lookup"><span data-stu-id="84a30-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="84a30-121"><dt>**CONECTAR \_ E \_ noconnection**</dt></span><span class="sxs-lookup"><span data-stu-id="84a30-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="84a30-122">No se encontró el receptor de notificaciones identificado por *TID* .</span><span class="sxs-lookup"><span data-stu-id="84a30-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="84a30-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84a30-123">Requirements</span></span>



| <span data-ttu-id="84a30-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a30-124">Requirement</span></span> | <span data-ttu-id="84a30-125">Value</span><span class="sxs-lookup"><span data-stu-id="84a30-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84a30-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84a30-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84a30-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="84a30-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84a30-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84a30-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84a30-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84a30-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="84a30-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="84a30-130">Redistributable</span></span><br/>          | <span data-ttu-id="84a30-131">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="84a30-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="84a30-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84a30-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a30-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a30-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="84a30-134">IDL</span><span class="sxs-lookup"><span data-stu-id="84a30-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84a30-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84a30-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="84a30-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84a30-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84a30-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84a30-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a30-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="84a30-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a30-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="84a30-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="84a30-140">ISoftKbd::AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="84a30-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





