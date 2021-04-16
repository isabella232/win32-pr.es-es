---
title: Mensaje de MCIWNDM_SETTIMEFORMAT (VFW. h)
description: El \_ mensaje MCIWNDM SETTIMEFORMAT establece el formato de hora de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- Mensaje de MCIWNDM_SETTIMEFORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533801"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="fd464-105">MCIWNDM \_ SETTIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="fd464-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="fd464-106">El mensaje **MCIWNDM \_ SETTIMEFORMAT** establece el formato de hora de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="fd464-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="fd464-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="fd464-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="fd464-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd464-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd464-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="fd464-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="fd464-110">Puntero a un búfer que contiene la cadena terminada en null que indica el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="fd464-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="fd464-111">Especifique "frames" para establecer el formato de hora en los marcos o "MS" para establecer el formato de hora en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="fd464-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd464-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd464-112">Return Value</span></span>

<span data-ttu-id="fd464-113">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fd464-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd464-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd464-114">Remarks</span></span>

<span data-ttu-id="fd464-115">Una aplicación puede especificar formatos de hora que no sean fotogramas o milisegundos, siempre que el dispositivo MCI admita los formatos.</span><span class="sxs-lookup"><span data-stu-id="fd464-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="fd464-116">Los formatos no continuos, como las pistas y SMPTE, pueden hacer que la barra de seguimiento se comporte de forma errática.</span><span class="sxs-lookup"><span data-stu-id="fd464-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="fd464-117">Para estos formatos de hora, puede que desee desactivar la barra de herramientas mediante la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) y especificar el estilo de \_ ventana MCIWNDF NOPLAYBAR.</span><span class="sxs-lookup"><span data-stu-id="fd464-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="fd464-118">Si desea establecer el formato de hora en fotogramas o milisegundos, también puede usar la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) o [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) .</span><span class="sxs-lookup"><span data-stu-id="fd464-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="fd464-119">Para obtener una lista de formatos de hora, vea la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="fd464-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd464-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd464-120">Requirements</span></span>



| <span data-ttu-id="fd464-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd464-121">Requirement</span></span> | <span data-ttu-id="fd464-122">Value</span><span class="sxs-lookup"><span data-stu-id="fd464-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fd464-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd464-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fd464-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd464-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fd464-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd464-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fd464-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd464-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fd464-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd464-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd464-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd464-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd464-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd464-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd464-130">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="fd464-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="fd464-131">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="fd464-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="fd464-132">**MCIWndSetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="fd464-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="fd464-133">**MCIWndUseFrames**</span><span class="sxs-lookup"><span data-stu-id="fd464-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="fd464-134">**MCIWndUseTime**</span><span class="sxs-lookup"><span data-stu-id="fd464-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





