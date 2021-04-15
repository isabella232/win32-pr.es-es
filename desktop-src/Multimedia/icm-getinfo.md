---
title: Mensaje de ICM_GETINFO (VFW. h)
description: El \_ mensaje GetInfo de ICM consulta un controlador de compresión de vídeo para devolver una descripción de sí mismo en una estructura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- Mensaje de ICM_GETINFO de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676776"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="527b7-104">\_Mensaje GetInfo de ICM</span><span class="sxs-lookup"><span data-stu-id="527b7-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="527b7-105">El **mensaje \_ GetInfo de ICM** consulta un controlador de compresión de vídeo para devolver una descripción de sí mismo en una estructura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="527b7-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="527b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="527b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527b7-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span><span class="sxs-lookup"><span data-stu-id="527b7-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="527b7-108">Puntero a una estructura **ICINFO** que contiene información.</span><span class="sxs-lookup"><span data-stu-id="527b7-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="527b7-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="527b7-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="527b7-110">Tamaño, en bytes, de **ICINFO**.</span><span class="sxs-lookup"><span data-stu-id="527b7-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="527b7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="527b7-111">Return Value</span></span>

<span data-ttu-id="527b7-112">Devuelve el tamaño, en bytes, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) o cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="527b7-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="527b7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="527b7-113">Remarks</span></span>

<span data-ttu-id="527b7-114">Normalmente, las aplicaciones envían este mensaje para mostrar una lista de los compresores instalados.</span><span class="sxs-lookup"><span data-stu-id="527b7-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="527b7-115">El controlador debe rellenar todos los miembros de la estructura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , excepto **szDriver**.</span><span class="sxs-lookup"><span data-stu-id="527b7-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="527b7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="527b7-116">Requirements</span></span>



| <span data-ttu-id="527b7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="527b7-117">Requirement</span></span> | <span data-ttu-id="527b7-118">Value</span><span class="sxs-lookup"><span data-stu-id="527b7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="527b7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="527b7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="527b7-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="527b7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="527b7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="527b7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="527b7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="527b7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="527b7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="527b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="527b7-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="527b7-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="527b7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="527b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527b7-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="527b7-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="527b7-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="527b7-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





