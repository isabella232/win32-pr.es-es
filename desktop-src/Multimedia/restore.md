---
title: comando restore
description: El comando restore copia una imagen fija de un archivo en el búfer de fotogramas. Este es el inverso del comando de captura. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- comando restore de Windows multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995956"
---
# <a name="restore-command"></a><span data-ttu-id="6742d-106">comando restore</span><span class="sxs-lookup"><span data-stu-id="6742d-106">restore command</span></span>

<span data-ttu-id="6742d-107">El comando restore copia una imagen fija de un archivo en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6742d-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="6742d-108">Este es el inverso del comando de [captura](capture.md) .</span><span class="sxs-lookup"><span data-stu-id="6742d-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="6742d-109">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="6742d-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="6742d-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="6742d-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6742d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6742d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6742d-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6742d-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6742d-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6742d-113">Identifier of an MCI device.</span></span> <span data-ttu-id="6742d-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6742d-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6742d-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span><span class="sxs-lookup"><span data-stu-id="6742d-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="6742d-116">Una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6742d-116">One or more of the following flags.</span></span>



| <span data-ttu-id="6742d-117">Value</span><span class="sxs-lookup"><span data-stu-id="6742d-117">Value</span></span>           | <span data-ttu-id="6742d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="6742d-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6742d-119">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="6742d-119">at *rectangle*</span></span>  | <span data-ttu-id="6742d-120">Especifica un rectángulo con respecto al origen de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6742d-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="6742d-121">El *rectángulo* se especifica como *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="6742d-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="6742d-122">Las coordenadas *x1 Y1* especifican la esquina superior izquierda y las coordenadas *x2 Y2* especifican el ancho y el alto. Si no se usa esta marca, la imagen se copia en la esquina superior izquierda del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6742d-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="6742d-123">desde *nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="6742d-123">from *filename*</span></span> | <span data-ttu-id="6742d-124">Especifica el nombre de archivo de la imagen que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6742d-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="6742d-125">Esta marca es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="6742d-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6742d-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="6742d-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6742d-127">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="6742d-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6742d-128">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6742d-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6742d-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6742d-129">Return Value</span></span>

<span data-ttu-id="6742d-130">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6742d-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6742d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6742d-131">Remarks</span></span>

<span data-ttu-id="6742d-132">Los dispositivos pueden reconocer una variedad de formatos de imagen; siempre se reconoce un mapa de bits independiente del dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="6742d-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6742d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6742d-133">Requirements</span></span>



| <span data-ttu-id="6742d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6742d-134">Requirement</span></span> | <span data-ttu-id="6742d-135">Value</span><span class="sxs-lookup"><span data-stu-id="6742d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6742d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6742d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6742d-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6742d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6742d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6742d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6742d-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6742d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6742d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6742d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6742d-141">MCI</span><span class="sxs-lookup"><span data-stu-id="6742d-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6742d-142">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="6742d-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="6742d-143">grabar</span><span class="sxs-lookup"><span data-stu-id="6742d-143">capture</span></span>](capture.md)
</dt> </dl>

 

