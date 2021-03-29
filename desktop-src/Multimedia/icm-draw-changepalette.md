---
title: Mensaje de ICM_DRAW_CHANGEPALETTE (VFW. h)
description: El mensaje CHANGEPALETTE de ICM de \_ Draw \_ notifica a un controlador de representación que la paleta de películas está cambiando. Puede enviar este mensaje explícitamente o mediante la macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- Mensaje de ICM_DRAW_CHANGEPALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905336"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="7f8a0-105">\_Mensaje CHANGEPALETTE de Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="7f8a0-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="7f8a0-106">El **mensaje \_ \_ CHANGEPALETTE de ICM de Draw** notifica a un controlador de representación que la paleta de películas está cambiando.</span><span class="sxs-lookup"><span data-stu-id="7f8a0-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="7f8a0-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .</span><span class="sxs-lookup"><span data-stu-id="7f8a0-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7f8a0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f8a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f8a0-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="7f8a0-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="7f8a0-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el nuevo formato y la tabla de colores opcional.</span><span class="sxs-lookup"><span data-stu-id="7f8a0-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f8a0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f8a0-111">Return Value</span></span>

<span data-ttu-id="7f8a0-112">Devuelve ICERR \_ OK si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7f8a0-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f8a0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f8a0-113">Remarks</span></span>

<span data-ttu-id="7f8a0-114">Este mensaje debe ser compatible con los controladores de representación instalables que dibujan DIB con una estructura interna que incluye una paleta.</span><span class="sxs-lookup"><span data-stu-id="7f8a0-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8a0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f8a0-115">Requirements</span></span>



| <span data-ttu-id="7f8a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f8a0-116">Requirement</span></span> | <span data-ttu-id="7f8a0-117">Value</span><span class="sxs-lookup"><span data-stu-id="7f8a0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7f8a0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f8a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8a0-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7f8a0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7f8a0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f8a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8a0-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f8a0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7f8a0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f8a0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f8a0-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f8a0-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8a0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f8a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8a0-125">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="7f8a0-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7f8a0-126">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="7f8a0-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

