---
title: Mensaje de MCIWNDM_GETMODE (VFW. h)
description: El \_ mensaje MCIWNDM GETMODE recupera el modo de funcionamiento actual de un dispositivo MCI. Los dispositivos MCI tienen varios modos operativos, que se designan mediante constantes. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- Mensaje de MCIWNDM_GETMODE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149874"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="e1786-106">MCIWNDM \_ GETMODE</span><span class="sxs-lookup"><span data-stu-id="e1786-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="e1786-107">El mensaje **MCIWNDM \_ GETMODE** recupera el modo de funcionamiento actual de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e1786-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="e1786-108">Los dispositivos MCI tienen varios modos operativos, que se designan mediante constantes.</span><span class="sxs-lookup"><span data-stu-id="e1786-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="e1786-109">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .</span><span class="sxs-lookup"><span data-stu-id="e1786-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="e1786-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1786-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1786-111"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="e1786-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="e1786-112">Tamaño, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="e1786-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e1786-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="e1786-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="e1786-114">Puntero al búfer definido por la aplicación que se usa para devolver el modo.</span><span class="sxs-lookup"><span data-stu-id="e1786-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1786-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1786-115">Return Value</span></span>

<span data-ttu-id="e1786-116">Devuelve un entero que corresponde a la constante de MCI que define el modo.</span><span class="sxs-lookup"><span data-stu-id="e1786-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1786-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1786-117">Remarks</span></span>

<span data-ttu-id="e1786-118">Si la cadena terminada en null que describe el modo es más larga que el búfer, se trunca.</span><span class="sxs-lookup"><span data-stu-id="e1786-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="e1786-119">No todos los dispositivos pueden funcionar en todos los modos.</span><span class="sxs-lookup"><span data-stu-id="e1786-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="e1786-120">Por ejemplo, el dispositivo MCIAVI es un dispositivo de reproducción; no es compatible con el modo de grabación.</span><span class="sxs-lookup"><span data-stu-id="e1786-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="e1786-121">Los siguientes modos se pueden recuperar mediante **MCIWNDM \_ GETMODE**.</span><span class="sxs-lookup"><span data-stu-id="e1786-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="e1786-122">Modo de funcionamiento</span><span class="sxs-lookup"><span data-stu-id="e1786-122">Operating mode</span></span> | <span data-ttu-id="e1786-123">MCI (constante)</span><span class="sxs-lookup"><span data-stu-id="e1786-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="e1786-124">no está listo</span><span class="sxs-lookup"><span data-stu-id="e1786-124">not ready</span></span>      | <span data-ttu-id="e1786-125">\_modo MCI \_ no \_ listo</span><span class="sxs-lookup"><span data-stu-id="e1786-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="e1786-126">abrir</span><span class="sxs-lookup"><span data-stu-id="e1786-126">open</span></span>           | <span data-ttu-id="e1786-127">\_modo MCI \_ abierto</span><span class="sxs-lookup"><span data-stu-id="e1786-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="e1786-128">en pausa</span><span class="sxs-lookup"><span data-stu-id="e1786-128">paused</span></span>         | <span data-ttu-id="e1786-129">\_pausar modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="e1786-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="e1786-130">reproducción</span><span class="sxs-lookup"><span data-stu-id="e1786-130">playing</span></span>        | <span data-ttu-id="e1786-131">\_reproducción en modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="e1786-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="e1786-132">grabación</span><span class="sxs-lookup"><span data-stu-id="e1786-132">recording</span></span>      | <span data-ttu-id="e1786-133">\_registro en modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="e1786-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="e1786-134">buscar</span><span class="sxs-lookup"><span data-stu-id="e1786-134">seeking</span></span>        | <span data-ttu-id="e1786-135">\_búsqueda en modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="e1786-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="e1786-136">stopped</span><span class="sxs-lookup"><span data-stu-id="e1786-136">stopped</span></span>        | <span data-ttu-id="e1786-137">\_detención del modo MCI \_</span><span class="sxs-lookup"><span data-stu-id="e1786-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="e1786-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1786-138">Requirements</span></span>



| <span data-ttu-id="e1786-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1786-139">Requirement</span></span> | <span data-ttu-id="e1786-140">Value</span><span class="sxs-lookup"><span data-stu-id="e1786-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1786-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1786-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e1786-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1786-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1786-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1786-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e1786-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1786-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1786-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1786-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1786-146"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1786-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1786-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1786-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1786-148">**MCIWndGetMode**</span><span class="sxs-lookup"><span data-stu-id="e1786-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





