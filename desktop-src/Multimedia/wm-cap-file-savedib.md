---
title: Mensaje de WM_CAP_FILE_SAVEDIB (VFW. h)
description: El \_ mensaje SAVEDIB del archivo Cap de WM \_ \_ copia el marco actual en un archivo DIB. Puede enviar este mensaje explícitamente o mediante la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- Mensaje de WM_CAP_FILE_SAVEDIB de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492952"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="bb700-105">\_ \_ Mensaje SAVEDIB de archivo Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="bb700-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="bb700-106">El **mensaje \_ \_ \_ SAVEDIB del archivo Cap de WM** copia el marco actual en un archivo DIB.</span><span class="sxs-lookup"><span data-stu-id="bb700-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="bb700-107">Puede enviar este mensaje explícitamente o mediante la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .</span><span class="sxs-lookup"><span data-stu-id="bb700-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="bb700-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb700-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb700-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="bb700-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="bb700-110">Puntero a la cadena terminada en null que contiene el nombre del archivo DIB de destino.</span><span class="sxs-lookup"><span data-stu-id="bb700-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb700-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb700-111">Return Value</span></span>

<span data-ttu-id="bb700-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb700-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="bb700-113">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="bb700-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb700-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb700-114">Remarks</span></span>

<span data-ttu-id="bb700-115">Si el controlador de captura proporciona fotogramas en un formato comprimido, esta llamada intenta descomprimir el marco antes de escribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="bb700-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb700-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb700-116">Requirements</span></span>



| <span data-ttu-id="bb700-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb700-117">Requirement</span></span> | <span data-ttu-id="bb700-118">Value</span><span class="sxs-lookup"><span data-stu-id="bb700-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb700-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb700-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb700-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb700-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bb700-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb700-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb700-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb700-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bb700-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb700-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb700-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb700-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb700-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb700-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb700-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="bb700-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bb700-127">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="bb700-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





