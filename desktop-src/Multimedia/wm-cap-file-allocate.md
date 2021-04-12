---
title: Mensaje de WM_CAP_FILE_ALLOCATE (VFW. h)
description: El \_ archivo de Cap de WM \_ \_ asignar mensaje crea (preasigna) un archivo de captura de un tamaño especificado. Puede enviar este mensaje explícitamente o mediante la macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- Mensaje de WM_CAP_FILE_ALLOCATE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489748"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="758f7-105">\_Mensaje de \_ asignación de archivo Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="758f7-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="758f7-106">El **archivo de Cap de WM \_ \_ \_ asignar** mensaje crea (preasigna) un archivo de captura de un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="758f7-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="758f7-107">Puede enviar este mensaje explícitamente o mediante la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .</span><span class="sxs-lookup"><span data-stu-id="758f7-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="758f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="758f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="758f7-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span><span class="sxs-lookup"><span data-stu-id="758f7-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="758f7-110">Tamaño, en bytes, para crear el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="758f7-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="758f7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="758f7-111">Return Value</span></span>

<span data-ttu-id="758f7-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="758f7-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="758f7-113">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="758f7-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="758f7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="758f7-114">Remarks</span></span>

<span data-ttu-id="758f7-115">Puede mejorar significativamente el rendimiento de la captura de transmisión por secuencias si asigna previamente un archivo de captura lo suficientemente grande como para almacenar un clip de vídeo completo y desfragmenta el archivo de captura antes de capturar el clip.</span><span class="sxs-lookup"><span data-stu-id="758f7-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="758f7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="758f7-116">Requirements</span></span>



| <span data-ttu-id="758f7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="758f7-117">Requirement</span></span> | <span data-ttu-id="758f7-118">Value</span><span class="sxs-lookup"><span data-stu-id="758f7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="758f7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="758f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="758f7-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="758f7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="758f7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="758f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="758f7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="758f7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="758f7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="758f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="758f7-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="758f7-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="758f7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="758f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758f7-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="758f7-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="758f7-127">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="758f7-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





