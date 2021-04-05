---
title: Mensaje de WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: El archivo Cap de WM establece el \_ \_ \_ conjunto \_ de mensajes INFOCHUNK y borra fragmentos de información.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- Mensaje de WM_CAP_FILE_SET_INFOCHUNK de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078898"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="04ec6-104">\_ \_ \_ Mensaje INFOCHUNK de conjunto de archivos Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="04ec6-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="04ec6-105">El **archivo Cap de WM establece el conjunto de mensajes \_ \_ \_ \_ INFOCHUNK** y borra fragmentos de información.</span><span class="sxs-lookup"><span data-stu-id="04ec6-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="04ec6-106">Se pueden insertar fragmentos de información en un archivo AVI durante la captura para insertar cadenas de texto o datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="04ec6-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="04ec6-107">Puede enviar este mensaje explícitamente o mediante la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="04ec6-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="04ec6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04ec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ec6-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span><span class="sxs-lookup"><span data-stu-id="04ec6-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="04ec6-110">Puntero a una estructura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) que define el fragmento de información que se va a crear o eliminar.</span><span class="sxs-lookup"><span data-stu-id="04ec6-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ec6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04ec6-111">Return Value</span></span>

<span data-ttu-id="04ec6-112">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="04ec6-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="04ec6-113">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="04ec6-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ec6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04ec6-114">Remarks</span></span>

<span data-ttu-id="04ec6-115">Se pueden agregar varios fragmentos de información registrados a un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="04ec6-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="04ec6-116">Después de establecer un fragmento de información, sigue siendo agregado a los archivos de captura posteriores hasta que se borre la entrada o se borren todas las entradas de fragmentos de información.</span><span class="sxs-lookup"><span data-stu-id="04ec6-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="04ec6-117">Para borrar una sola entrada, especifique el fragmento de información en el miembro **fccInfoID** y **null** en el miembro **lpData** de la estructura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="04ec6-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="04ec6-118">Para borrar todas las entradas, especifique **null** en **fccInfoID**.</span><span class="sxs-lookup"><span data-stu-id="04ec6-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ec6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ec6-119">Requirements</span></span>



| <span data-ttu-id="04ec6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ec6-120">Requirement</span></span> | <span data-ttu-id="04ec6-121">Value</span><span class="sxs-lookup"><span data-stu-id="04ec6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="04ec6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ec6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04ec6-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04ec6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="04ec6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ec6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04ec6-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04ec6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="04ec6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04ec6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ec6-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ec6-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ec6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="04ec6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ec6-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="04ec6-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="04ec6-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="04ec6-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





