---
title: Mensaje de ICM_DRAW_REALIZE (VFW. h)
description: El mensaje de presentación de ICM de ICM \_ \_ notifica a un controlador de representación que debe observar su paleta de dibujo durante el dibujo. Puede enviar este mensaje explícitamente o mediante la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- Mensaje de ICM_DRAW_REALIZE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422227"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="b480b-105">Mensaje de error de \_ Draw de ICM \_</span><span class="sxs-lookup"><span data-stu-id="b480b-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="b480b-106">El mensaje de presentación de **ICM de ICM \_ \_** notifica a un controlador de representación que debe observar su paleta de dibujo durante el dibujo.</span><span class="sxs-lookup"><span data-stu-id="b480b-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="b480b-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .</span><span class="sxs-lookup"><span data-stu-id="b480b-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="b480b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b480b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b480b-109"><span id="hdc"></span><span id="HDC"></span>*cámaras*</span><span class="sxs-lookup"><span data-stu-id="b480b-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="b480b-110">Identificador del controlador de dominio usado para obtener la paleta.</span><span class="sxs-lookup"><span data-stu-id="b480b-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="b480b-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span><span class="sxs-lookup"><span data-stu-id="b480b-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="b480b-112">Marca de fondo.</span><span class="sxs-lookup"><span data-stu-id="b480b-112">Background flag.</span></span> <span data-ttu-id="b480b-113">Especifique **true** para obtener la paleta como una tarea en segundo plano o **false** para obtener la paleta en primer plano.</span><span class="sxs-lookup"><span data-stu-id="b480b-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b480b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b480b-114">Return Value</span></span>

<span data-ttu-id="b480b-115">Devuelve ICERR \_ OK si se realiza la paleta de dibujo o \_ no se admite ICERR si se realiza la paleta asociada a los datos descomprimidos.</span><span class="sxs-lookup"><span data-stu-id="b480b-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="b480b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b480b-116">Remarks</span></span>

<span data-ttu-id="b480b-117">Los controladores deben responder a este mensaje solo si la paleta de dibujo es diferente de la paleta descomprimida.</span><span class="sxs-lookup"><span data-stu-id="b480b-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="b480b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b480b-118">Requirements</span></span>



| <span data-ttu-id="b480b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b480b-119">Requirement</span></span> | <span data-ttu-id="b480b-120">Value</span><span class="sxs-lookup"><span data-stu-id="b480b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b480b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b480b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b480b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b480b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b480b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b480b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b480b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b480b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b480b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b480b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b480b-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b480b-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b480b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b480b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b480b-128">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="b480b-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b480b-129">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="b480b-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





