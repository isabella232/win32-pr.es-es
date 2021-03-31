---
title: Mensaje de MCIWNDM_GETTIMEFORMAT (VFW. h)
description: El \_ mensaje MCIWNDM GETTIMEFORMAT recupera el formato de hora actual de un dispositivo MCI en dos formatos como un valor numérico y como una cadena. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- Mensaje de MCIWNDM_GETTIMEFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801328"
---
# <a name="mciwndm_gettimeformat-message"></a><span data-ttu-id="a4eb6-105">MCIWNDM \_ GETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a4eb6-105">MCIWNDM\_GETTIMEFORMAT message</span></span>

<span data-ttu-id="a4eb6-106">El mensaje **MCIWNDM \_ GETTIMEFORMAT** recupera el formato de hora actual de un dispositivo MCI en dos formatos: como valor numérico y como cadena.</span><span class="sxs-lookup"><span data-stu-id="a4eb6-106">The **MCIWNDM\_GETTIMEFORMAT** message retrieves the current time format of an MCI device in two forms: as a numerical value and as a string.</span></span> <span data-ttu-id="a4eb6-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="a4eb6-107">You can send this message explicitly or by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="a4eb6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4eb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4eb6-109"><span id="len"></span><span id="LEN"></span>*terminado*</span><span class="sxs-lookup"><span data-stu-id="a4eb6-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="a4eb6-110">Tamaño, en bytes, del búfer.</span><span class="sxs-lookup"><span data-stu-id="a4eb6-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a4eb6-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="a4eb6-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="a4eb6-112">Puntero a un búfer que va a contener la forma de cadena terminada en NULL del formato de hora.</span><span class="sxs-lookup"><span data-stu-id="a4eb6-112">Pointer to a buffer to contain the null-terminated string form of the time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4eb6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4eb6-113">Return Value</span></span>

<span data-ttu-id="a4eb6-114">Devuelve un entero que corresponde a la constante de MCI que define el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="a4eb6-114">Returns an integer corresponding to the MCI constant defining the time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4eb6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4eb6-115">Remarks</span></span>

<span data-ttu-id="a4eb6-116">Si la cadena de formato de hora es mayor que el búfer de retorno, MCIWnd trunca la cadena.</span><span class="sxs-lookup"><span data-stu-id="a4eb6-116">If the time format string is longer than the return buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="a4eb6-117">Un dispositivo MCI puede admitir uno o varios de los siguientes formatos de hora.</span><span class="sxs-lookup"><span data-stu-id="a4eb6-117">An MCI device can support one or more of the following time formats.</span></span>



| <span data-ttu-id="a4eb6-118">Formato de hora</span><span class="sxs-lookup"><span data-stu-id="a4eb6-118">Time format</span></span>                      | <span data-ttu-id="a4eb6-119">MCI (constante)</span><span class="sxs-lookup"><span data-stu-id="a4eb6-119">MCI constant</span></span>               |
|----------------------------------|----------------------------|
| <span data-ttu-id="a4eb6-120">Bytes</span><span class="sxs-lookup"><span data-stu-id="a4eb6-120">Bytes</span></span>                            | <span data-ttu-id="a4eb6-121">\_bytes de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="a4eb6-121">MCI\_FORMAT\_BYTES</span></span>         |
| <span data-ttu-id="a4eb6-122">Imágenes</span><span class="sxs-lookup"><span data-stu-id="a4eb6-122">Frames</span></span>                           | <span data-ttu-id="a4eb6-123">\_marcos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="a4eb6-123">MCI\_FORMAT\_FRAMES</span></span>        |
| <span data-ttu-id="a4eb6-124">Horas, minutos, segundos</span><span class="sxs-lookup"><span data-stu-id="a4eb6-124">Hours, minutes, seconds</span></span>          | <span data-ttu-id="a4eb6-125">\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="a4eb6-125">MCI\_FORMAT\_HMS</span></span>           |
| <span data-ttu-id="a4eb6-126">Milisegundos</span><span class="sxs-lookup"><span data-stu-id="a4eb6-126">Milliseconds</span></span>                     | <span data-ttu-id="a4eb6-127">formato MCI en \_ \_ milisegundos</span><span class="sxs-lookup"><span data-stu-id="a4eb6-127">MCI\_FORMAT\_MILLISECONDS</span></span>  |
| <span data-ttu-id="a4eb6-128">Minutos, segundos, fotogramas</span><span class="sxs-lookup"><span data-stu-id="a4eb6-128">Minutes, seconds, frames</span></span>         | <span data-ttu-id="a4eb6-129">\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="a4eb6-129">MCI\_FORMAT\_MSF</span></span>           |
| <span data-ttu-id="a4eb6-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a4eb6-130">Samples</span></span>                          | <span data-ttu-id="a4eb6-131">\_ejemplos de formato de MCI \_</span><span class="sxs-lookup"><span data-stu-id="a4eb6-131">MCI\_FORMAT\_SAMPLES</span></span>       |
| <span data-ttu-id="a4eb6-132">SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="a4eb6-132">SMPTE 24</span></span>                         | <span data-ttu-id="a4eb6-133">\_Formato MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="a4eb6-133">MCI\_FORMAT\_SMPTE\_24</span></span>     |
| <span data-ttu-id="a4eb6-134">SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="a4eb6-134">SMPTE 25</span></span>                         | <span data-ttu-id="a4eb6-135">\_Formato MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="a4eb6-135">MCI\_FORMAT\_SMPTE\_25</span></span>     |
| <span data-ttu-id="a4eb6-136">Eliminación SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="a4eb6-136">SMPTE 30 drop</span></span>                    | <span data-ttu-id="a4eb6-137">\_Formato MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="a4eb6-137">MCI\_FORMAT\_SMPTE\_30DROP</span></span> |
| <span data-ttu-id="a4eb6-138">SMPTE 30 (no Drop)</span><span class="sxs-lookup"><span data-stu-id="a4eb6-138">SMPTE 30 (non-drop)</span></span>              | <span data-ttu-id="a4eb6-139">\_Formato MCI \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="a4eb6-139">MCI\_FORMAT\_SMPTE\_30</span></span>     |
| <span data-ttu-id="a4eb6-140">Pistas, minutos, segundos, fotogramas</span><span class="sxs-lookup"><span data-stu-id="a4eb6-140">Tracks, minutes, seconds, frames</span></span> | <span data-ttu-id="a4eb6-141">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="a4eb6-141">MCI\_FORMAT\_TMSF</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="a4eb6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4eb6-142">Requirements</span></span>



| <span data-ttu-id="a4eb6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4eb6-143">Requirement</span></span> | <span data-ttu-id="a4eb6-144">Value</span><span class="sxs-lookup"><span data-stu-id="a4eb6-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a4eb6-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4eb6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a4eb6-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a4eb6-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a4eb6-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4eb6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a4eb6-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4eb6-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a4eb6-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4eb6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4eb6-150"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4eb6-150"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4eb6-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4eb6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4eb6-152">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="a4eb6-152">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





