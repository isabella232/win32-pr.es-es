---
title: Mensaje de WM_CAP_DRIVER_GET_NAME (VFW. h)
description: El \_ mensaje del \_ controlador de Cap de WM \_ Get \_ Name devuelve el nombre del controlador de captura conectado a la ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- Mensaje de WM_CAP_DRIVER_GET_NAME de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489749"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="57539-105">\_Mensaje de \_ obtención \_ de \_ nombre de controlador Cap de WM</span><span class="sxs-lookup"><span data-stu-id="57539-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="57539-106">El mensaje del **controlador de Cap de WM \_ \_ \_ Get \_ Name** devuelve el nombre del controlador de captura conectado a la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="57539-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="57539-107">Puede enviar este mensaje explícitamente o mediante la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .</span><span class="sxs-lookup"><span data-stu-id="57539-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="57539-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57539-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57539-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="57539-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="57539-110">Tamaño, en bytes, del búfer al que se hace referencia en **szName**.</span><span class="sxs-lookup"><span data-stu-id="57539-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="57539-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="57539-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="57539-112">Puntero a un búfer definido por la aplicación que se usa para devolver el nombre del dispositivo como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="57539-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57539-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57539-113">Return Value</span></span>

<span data-ttu-id="57539-114">Devuelve **true** si es correcto o **false** si la ventana de captura no está conectada a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="57539-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="57539-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57539-115">Remarks</span></span>

<span data-ttu-id="57539-116">El nombre es una cadena de texto que se recupera del área de recursos del controlador.</span><span class="sxs-lookup"><span data-stu-id="57539-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="57539-117">Las aplicaciones deben asignar aproximadamente 80 bytes para esta cadena.</span><span class="sxs-lookup"><span data-stu-id="57539-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="57539-118">Si el controlador no contiene un recurso de nombre, se devuelve el nombre completo de la ruta de acceso del controlador enumerado en el registro o en el archivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="57539-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="57539-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57539-119">Requirements</span></span>



| <span data-ttu-id="57539-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57539-120">Requirement</span></span> | <span data-ttu-id="57539-121">Value</span><span class="sxs-lookup"><span data-stu-id="57539-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57539-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57539-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57539-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="57539-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57539-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57539-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57539-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="57539-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57539-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57539-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57539-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="57539-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57539-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="57539-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57539-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="57539-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="57539-130">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="57539-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





