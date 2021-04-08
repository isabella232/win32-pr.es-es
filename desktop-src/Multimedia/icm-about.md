---
title: Mensaje de ICM_ABOUT (VFW. h)
description: El \_ mensaje acerca de ICM informa a un controlador de compresión de vídeo para que muestre su cuadro de diálogo acerca de o consulta un controlador de compresión de vídeo para determinar si tiene el cuadro de diálogo acerca de. Puede enviar este mensaje explícitamente o mediante la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- Mensaje de ICM_ABOUT de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078843"
---
# <a name="icm_about-message"></a><span data-ttu-id="3f1cc-105">\_Mensaje acerca de ICM</span><span class="sxs-lookup"><span data-stu-id="3f1cc-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="3f1cc-106">El **mensaje \_ acerca de ICM** informa a un controlador de compresión de vídeo para que muestre su cuadro de diálogo acerca de o consulta un controlador de compresión de vídeo para determinar si tiene el cuadro de diálogo acerca de.</span><span class="sxs-lookup"><span data-stu-id="3f1cc-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="3f1cc-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .</span><span class="sxs-lookup"><span data-stu-id="3f1cc-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3f1cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f1cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f1cc-109"><span id="hwnd"></span><span id="HWND"></span>*identificador*</span><span class="sxs-lookup"><span data-stu-id="3f1cc-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="3f1cc-110">Identificador de la ventana primaria del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3f1cc-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="3f1cc-111">También puede determinar si un controlador tiene un cuadro de diálogo acerca de especificando-1 en este parámetro, como en la macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) .</span><span class="sxs-lookup"><span data-stu-id="3f1cc-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="3f1cc-112">El controlador devuelve ICERR \_ OK si tiene un cuadro de diálogo about o ICERR \_ no admitido de otro modo.</span><span class="sxs-lookup"><span data-stu-id="3f1cc-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f1cc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f1cc-113">Return Value</span></span>

<span data-ttu-id="3f1cc-114">Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3f1cc-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f1cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f1cc-115">Requirements</span></span>



| <span data-ttu-id="3f1cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f1cc-116">Requirement</span></span> | <span data-ttu-id="3f1cc-117">Value</span><span class="sxs-lookup"><span data-stu-id="3f1cc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3f1cc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f1cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f1cc-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3f1cc-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3f1cc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f1cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f1cc-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f1cc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3f1cc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f1cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f1cc-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f1cc-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f1cc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f1cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1cc-125">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="3f1cc-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3f1cc-126">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="3f1cc-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





