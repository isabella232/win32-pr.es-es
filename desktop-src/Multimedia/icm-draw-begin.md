---
title: Mensaje de ICM_DRAW_BEGIN (VFW. h)
description: El mensaje de inicio de Draw de ICM \_ notifica a \_ un controlador de representación que debe prepararse para dibujar los datos.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- Mensaje de ICM_DRAW_BEGIN de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996895"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="3fd26-104">Mensaje de inicio de \_ dibujo ICM \_</span><span class="sxs-lookup"><span data-stu-id="3fd26-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="3fd26-105">El mensaje de **\_ \_ Inicio de Draw de ICM** notifica a un controlador de representación que debe prepararse para dibujar los datos.</span><span class="sxs-lookup"><span data-stu-id="3fd26-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="3fd26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fd26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd26-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span><span class="sxs-lookup"><span data-stu-id="3fd26-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="3fd26-108">Puntero a una estructura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="3fd26-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="3fd26-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fd26-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3fd26-110">Tamaño, en bytes, de **ICDRAWBEGIN**.</span><span class="sxs-lookup"><span data-stu-id="3fd26-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd26-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fd26-111">Return Value</span></span>

<span data-ttu-id="3fd26-112">Devuelve ICERR \_ OK si el controlador permite dibujar los datos en la pantalla de la forma y el formato especificados, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3fd26-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="3fd26-113">Entre los posibles valores de error se incluyen los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3fd26-113">Possible error values include the following.</span></span>



| <span data-ttu-id="3fd26-114">Value</span><span class="sxs-lookup"><span data-stu-id="3fd26-114">Value</span></span>               | <span data-ttu-id="3fd26-115">Significado</span><span class="sxs-lookup"><span data-stu-id="3fd26-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3fd26-116">ICERR \_ BADFORMAT</span><span class="sxs-lookup"><span data-stu-id="3fd26-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="3fd26-117">No se admite el formato de entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="3fd26-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="3fd26-118">ICERR \_ NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="3fd26-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="3fd26-119">El controlador no dibuja directamente en la pantalla o no admite este mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fd26-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3fd26-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fd26-120">Remarks</span></span>

<span data-ttu-id="3fd26-121">Si desea que el controlador Descomprima los datos en un búfer, envíe el mensaje de [**\_ \_ Inicio de descompresión ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd26-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="3fd26-122">Los mensajes de **\_ \_ Inicio de dibujo de ICM** y [**\_ \_ fin de dibujo de ICM**](icm-draw-end.md) no se anidan.</span><span class="sxs-lookup"><span data-stu-id="3fd26-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="3fd26-123">Si el controlador recibe **el \_ \_ Inicio de Draw de ICM** antes de que se detenga la descompresión con el **\_ \_ extremo de Draw ICM**, debe reiniciar la descompresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="3fd26-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd26-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd26-124">Requirements</span></span>



| <span data-ttu-id="3fd26-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd26-125">Requirement</span></span> | <span data-ttu-id="3fd26-126">Value</span><span class="sxs-lookup"><span data-stu-id="3fd26-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3fd26-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fd26-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd26-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3fd26-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3fd26-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fd26-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd26-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3fd26-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3fd26-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fd26-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd26-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd26-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd26-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fd26-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd26-134">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="3fd26-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3fd26-135">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="3fd26-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





