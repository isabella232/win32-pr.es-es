---
title: Mensaje de ICM_DRAW_QUERY (VFW. h)
description: El mensaje de consulta de dibujo de ICM consulta \_ \_ un controlador de representación para determinar si puede representar datos en un formato específico. Puede enviar este mensaje explícitamente o mediante la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- Mensaje de ICM_DRAW_QUERY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491147"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="7a5bb-105">Mensaje de consulta de \_ Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="7a5bb-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="7a5bb-106">El mensaje de **\_ \_ consulta de dibujo de ICM** consulta un controlador de representación para determinar si puede representar datos en un formato específico.</span><span class="sxs-lookup"><span data-stu-id="7a5bb-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="7a5bb-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="7a5bb-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7a5bb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a5bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5bb-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="7a5bb-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="7a5bb-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="7a5bb-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5bb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a5bb-111">Return Value</span></span>

<span data-ttu-id="7a5bb-112">Devuelve ICERR \_ OK si el controlador puede representar datos en el formato especificado o ICERR \_ BADFORMAT de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="7a5bb-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a5bb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a5bb-113">Remarks</span></span>

<span data-ttu-id="7a5bb-114">Este mensaje difiere del mensaje [**de \_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) en que consulta el controlador en un sentido general.</span><span class="sxs-lookup"><span data-stu-id="7a5bb-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="7a5bb-115">**ICM \_ \_Empezar a dibujar** determina si el controlador puede dibujar los datos con el formato especificado en condiciones específicas, como la ampliación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7a5bb-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5bb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a5bb-116">Requirements</span></span>



| <span data-ttu-id="7a5bb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a5bb-117">Requirement</span></span> | <span data-ttu-id="7a5bb-118">Value</span><span class="sxs-lookup"><span data-stu-id="7a5bb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7a5bb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a5bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5bb-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7a5bb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7a5bb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a5bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5bb-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a5bb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7a5bb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a5bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5bb-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5bb-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5bb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a5bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5bb-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="7a5bb-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7a5bb-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="7a5bb-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

