---
title: comando de captura
description: El comando Capture copia el contenido del búfer de Marcos y lo almacena en el archivo especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- comando de captura de Windows multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151032"
---
# <a name="capture-command"></a><span data-ttu-id="8d9c0-105">comando de captura</span><span class="sxs-lookup"><span data-stu-id="8d9c0-105">capture command</span></span>

<span data-ttu-id="8d9c0-106">El comando Capture copia el contenido del búfer de Marcos y lo almacena en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="8d9c0-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8d9c0-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8d9c0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d9c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9c0-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8d9c0-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8d9c0-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8d9c0-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8d9c0-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span><span class="sxs-lookup"><span data-stu-id="8d9c0-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="8d9c0-114">Una o varias de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8d9c0-114">One or more of the following flags:</span></span>



| <span data-ttu-id="8d9c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="8d9c0-115">Value</span></span>          | <span data-ttu-id="8d9c0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8d9c0-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9c0-117">como *nombreruta*</span><span class="sxs-lookup"><span data-stu-id="8d9c0-117">as *pathname*</span></span>  | <span data-ttu-id="8d9c0-118">Especifica la ruta de acceso de destino y el nombre de archivo de la imagen capturada.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="8d9c0-119">Esta marca es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="8d9c0-120">en el *rectángulo*</span><span class="sxs-lookup"><span data-stu-id="8d9c0-120">at *rectangle*</span></span> | <span data-ttu-id="8d9c0-121">Especifica la región rectangular dentro del búfer de fotogramas que el dispositivo recorta y guarda en el disco.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="8d9c0-122">Si se omite, la región recortada tiene como valor predeterminado el rectángulo especificado o predeterminado en un comando [Put](put.md) "Source" anterior para esta instancia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8d9c0-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8d9c0-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8d9c0-124">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="8d9c0-125">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8d9c0-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9c0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d9c0-126">Return Value</span></span>

<span data-ttu-id="8d9c0-127">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9c0-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d9c0-128">Remarks</span></span>

<span data-ttu-id="8d9c0-129">Este comando podría producir un error si el dispositivo está reproduciendo el vídeo de movimiento o ejecuta otra operación que consume muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="8d9c0-130">Si el búfer de fotogramas se actualiza en tiempo real, la actualización se pausa momentáneamente para que se capture una imagen completa.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="8d9c0-131">Si el dispositivo pone en pausa la actualización, puede haber un efecto visual o audible.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="8d9c0-132">Si no se han establecido el formato de archivo, el algoritmo de compresión y los niveles de calidad, se usan los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="8d9c0-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9c0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d9c0-133">Requirements</span></span>



| <span data-ttu-id="8d9c0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d9c0-134">Requirement</span></span> | <span data-ttu-id="8d9c0-135">Value</span><span class="sxs-lookup"><span data-stu-id="8d9c0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8d9c0-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d9c0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9c0-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8d9c0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d9c0-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d9c0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9c0-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d9c0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8d9c0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d9c0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9c0-141">MCI</span><span class="sxs-lookup"><span data-stu-id="8d9c0-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8d9c0-142">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="8d9c0-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="8d9c0-143">pondrán</span><span class="sxs-lookup"><span data-stu-id="8d9c0-143">put</span></span>](put.md)
</dt> </dl>

 

