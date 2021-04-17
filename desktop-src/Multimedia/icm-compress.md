---
title: Mensaje de ICM_COMPRESS (VFW. h)
description: El \_ mensaje de compresión ICM notifica a un controlador de compresión de vídeo que debe comprimir un fotograma de datos en un búfer definido por la aplicación.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- Mensaje de ICM_COMPRESS de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651412"
---
# <a name="icm_compress-message"></a><span data-ttu-id="2a42d-104">\_Mensaje de compresión ICM</span><span class="sxs-lookup"><span data-stu-id="2a42d-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="2a42d-105">El **mensaje \_ de compresión ICM** notifica a un controlador de compresión de vídeo que debe comprimir un fotograma de datos en un búfer definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a42d-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="2a42d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a42d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a42d-107"><span id="icc"></span><span id="ICC"></span>*ICC*</span><span class="sxs-lookup"><span data-stu-id="2a42d-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="2a42d-108">Puntero a una estructura [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) .</span><span class="sxs-lookup"><span data-stu-id="2a42d-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="2a42d-109">Los siguientes miembros de esta estructura especifican los parámetros de compresión: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** y **dwQuality**.</span><span class="sxs-lookup"><span data-stu-id="2a42d-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="2a42d-110">El controlador también debe utilizar el miembro **biSizeImage** de la estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) asociada a **lpbiOutput** de **ICCOMPRESS** para devolver el tamaño del fotograma comprimido.</span><span class="sxs-lookup"><span data-stu-id="2a42d-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="2a42d-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a42d-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2a42d-112">Tamaño, en bytes, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span><span class="sxs-lookup"><span data-stu-id="2a42d-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a42d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a42d-113">Return Value</span></span>

<span data-ttu-id="2a42d-114">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2a42d-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a42d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a42d-115">Requirements</span></span>



| <span data-ttu-id="2a42d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a42d-116">Requirement</span></span> | <span data-ttu-id="2a42d-117">Value</span><span class="sxs-lookup"><span data-stu-id="2a42d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a42d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a42d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2a42d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2a42d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a42d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a42d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2a42d-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a42d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a42d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a42d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a42d-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a42d-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a42d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a42d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a42d-125">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a42d-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2a42d-126">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a42d-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

