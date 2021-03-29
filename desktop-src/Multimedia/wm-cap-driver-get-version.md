---
title: Mensaje de WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: El \_ \_ mensaje de versión del controlador de Cap de WM \_ obtiene \_ la información de versión del controlador de captura conectado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- Mensaje de WM_CAP_DRIVER_GET_VERSION de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666061"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="90842-105">\_Mensaje de \_ obtención \_ de \_ versión del controlador Cap de WM</span><span class="sxs-lookup"><span data-stu-id="90842-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="90842-106">El mensaje de **versión del controlador de Cap de WM \_ \_ \_ obtiene \_** la información de versión del controlador de captura conectado a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="90842-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="90842-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .</span><span class="sxs-lookup"><span data-stu-id="90842-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="90842-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90842-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90842-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="90842-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="90842-110">Tamaño, en bytes, del búfer definido por la aplicación al que hace referencia **szVer**.</span><span class="sxs-lookup"><span data-stu-id="90842-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="90842-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span><span class="sxs-lookup"><span data-stu-id="90842-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="90842-112">Puntero a un búfer definido por la aplicación que se usa para devolver la información de versión como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="90842-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90842-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90842-113">Return Value</span></span>

<span data-ttu-id="90842-114">Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="90842-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="90842-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90842-115">Remarks</span></span>

<span data-ttu-id="90842-116">La información de versión es una cadena de texto que se recupera del área de recursos del controlador.</span><span class="sxs-lookup"><span data-stu-id="90842-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="90842-117">Las aplicaciones deben asignar aproximadamente 40 bytes para esta cadena.</span><span class="sxs-lookup"><span data-stu-id="90842-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="90842-118">Si la información de versión no está disponible, se devuelve una cadena **nula** .</span><span class="sxs-lookup"><span data-stu-id="90842-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="90842-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90842-119">Requirements</span></span>



| <span data-ttu-id="90842-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="90842-120">Requirement</span></span> | <span data-ttu-id="90842-121">Value</span><span class="sxs-lookup"><span data-stu-id="90842-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="90842-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90842-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90842-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90842-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="90842-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90842-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90842-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90842-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="90842-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90842-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="90842-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="90842-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90842-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="90842-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90842-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="90842-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="90842-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="90842-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





