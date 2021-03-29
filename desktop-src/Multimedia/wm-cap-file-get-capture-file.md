---
title: Mensaje de WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: El \_ mensaje de archivo Cap de WM \_ \_ Get \_ Capture \_ file devuelve el nombre del archivo de captura actual. Puede enviar este mensaje explícitamente o mediante la macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- Mensaje de WM_CAP_FILE_GET_CAPTURE_FILE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905051"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="2e3ae-105">\_Mensaje de \_ obtención \_ de \_ \_ archivo de Cap de WM</span><span class="sxs-lookup"><span data-stu-id="2e3ae-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="2e3ae-106">El mensaje de archivo **Cap de WM \_ \_ \_ Get \_ Capture \_ File** devuelve el nombre del archivo de captura actual.</span><span class="sxs-lookup"><span data-stu-id="2e3ae-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="2e3ae-107">Puede enviar este mensaje explícitamente o mediante la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="2e3ae-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="2e3ae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e3ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3ae-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="2e3ae-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="2e3ae-110">Tamaño, en bytes, del búfer definido por la aplicación al que se hace referencia en **szName**.</span><span class="sxs-lookup"><span data-stu-id="2e3ae-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="2e3ae-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="2e3ae-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="2e3ae-112">Puntero a un búfer definido por la aplicación que se usa para devolver el nombre del archivo de captura como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="2e3ae-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3ae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e3ae-113">Return Value</span></span>

<span data-ttu-id="2e3ae-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2e3ae-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e3ae-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e3ae-115">Remarks</span></span>

<span data-ttu-id="2e3ae-116">El nombre de archivo de captura predeterminado es C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="2e3ae-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3ae-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e3ae-117">Requirements</span></span>



| <span data-ttu-id="2e3ae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e3ae-118">Requirement</span></span> | <span data-ttu-id="2e3ae-119">Value</span><span class="sxs-lookup"><span data-stu-id="2e3ae-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ae-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e3ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3ae-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e3ae-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2e3ae-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e3ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3ae-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e3ae-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2e3ae-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e3ae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e3ae-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ae-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e3ae-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e3ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e3ae-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2e3ae-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2e3ae-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2e3ae-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





