---
title: Mensaje de MCIWNDM_SETZOOM (VFW. h)
description: El \_ mensaje MCIWNDM SETZOOM cambia el tamaño de una imagen de vídeo según un factor de zoom. Este marco ajusta el tamaño de una ventana de MCIWnd mientras mantiene una relación de aspecto constante. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- Mensaje de MCIWNDM_SETZOOM de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489407"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="a4f5a-106">MCIWNDM \_ SETZOOM</span><span class="sxs-lookup"><span data-stu-id="a4f5a-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="a4f5a-107">El mensaje **MCIWNDM \_ SETZOOM** cambia el tamaño de una imagen de vídeo según un factor de zoom.</span><span class="sxs-lookup"><span data-stu-id="a4f5a-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="a4f5a-108">Este marco ajusta el tamaño de una ventana de MCIWnd mientras mantiene una relación de aspecto constante.</span><span class="sxs-lookup"><span data-stu-id="a4f5a-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="a4f5a-109">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="a4f5a-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="a4f5a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4f5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f5a-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span><span class="sxs-lookup"><span data-stu-id="a4f5a-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="a4f5a-112">Factor de zoom expresado como porcentaje de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="a4f5a-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="a4f5a-113">Especifique 100 para mostrar la imagen en su tamaño creado, 200 para mostrar la imagen con el doble de tamaño normal, o 50 para mostrar la imagen a la mitad del tamaño normal.</span><span class="sxs-lookup"><span data-stu-id="a4f5a-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f5a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4f5a-114">Return Value</span></span>

<span data-ttu-id="a4f5a-115">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a4f5a-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f5a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f5a-116">Requirements</span></span>



| <span data-ttu-id="a4f5a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f5a-117">Requirement</span></span> | <span data-ttu-id="a4f5a-118">Value</span><span class="sxs-lookup"><span data-stu-id="a4f5a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a4f5a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4f5a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f5a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a4f5a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a4f5a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4f5a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f5a-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4f5a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a4f5a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4f5a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f5a-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f5a-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f5a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4f5a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f5a-126">**MCIWndSetZoom**</span><span class="sxs-lookup"><span data-stu-id="a4f5a-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





