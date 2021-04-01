---
title: Mensaje de WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: El \_ mensaje del \_ archivo de captura del \_ conjunto \_ de archivos de Cap de WM \_ nombra el archivo que se utiliza para la captura de vídeo. Puede enviar este mensaje explícitamente o mediante la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- Mensaje de WM_CAP_FILE_SET_CAPTURE_FILE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995910"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="7d148-105">\_Mensaje de \_ \_ archivo de captura de conjunto de archivos Cap \_ de WM \_</span><span class="sxs-lookup"><span data-stu-id="7d148-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="7d148-106">El mensaje del archivo de captura del conjunto de archivos de Cap de WM nombra el archivo que se utiliza para la captura de vídeo. **\_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d148-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="7d148-107">Puede enviar este mensaje explícitamente o mediante la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="7d148-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="7d148-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d148-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="7d148-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="7d148-110">Puntero a la cadena terminada en null que contiene el nombre del archivo de captura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7d148-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d148-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d148-111">Return Value</span></span>

<span data-ttu-id="7d148-112">Devuelve **true** si es correcto o **false** si el nombre de archivo no es válido o si la captura de streaming o de un solo fotograma está en curso.</span><span class="sxs-lookup"><span data-stu-id="7d148-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d148-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d148-113">Remarks</span></span>

<span data-ttu-id="7d148-114">Este mensaje almacena el nombre de archivo en una estructura interna.</span><span class="sxs-lookup"><span data-stu-id="7d148-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="7d148-115">No crea, asigna ni abre el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7d148-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="7d148-116">El nombre de archivo de captura predeterminado es C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="7d148-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d148-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d148-117">Requirements</span></span>



| <span data-ttu-id="7d148-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d148-118">Requirement</span></span> | <span data-ttu-id="7d148-119">Value</span><span class="sxs-lookup"><span data-stu-id="7d148-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7d148-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d148-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d148-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7d148-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7d148-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d148-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d148-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d148-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7d148-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d148-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d148-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d148-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d148-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d148-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d148-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7d148-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7d148-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7d148-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





