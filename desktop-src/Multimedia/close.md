---
title: comando cerrar (Corecrt \_ IO. h)
description: El comando cerrar cierra el dispositivo o el archivo y los recursos asociados. MCI descarga un dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- comando cerrar Windows multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996272"
---
# <a name="close-command"></a><span data-ttu-id="ad063-106">Close (comando)</span><span class="sxs-lookup"><span data-stu-id="ad063-106">close command</span></span>

<span data-ttu-id="ad063-107">El comando cerrar cierra el dispositivo o el archivo y los recursos asociados.</span><span class="sxs-lookup"><span data-stu-id="ad063-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="ad063-108">MCI descarga un dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="ad063-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="ad063-109">Todos los dispositivos MCI reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="ad063-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="ad063-110">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ad063-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ad063-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad063-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad063-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ad063-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ad063-113">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ad063-113">Identifier of an MCI device.</span></span> <span data-ttu-id="ad063-114">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad063-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ad063-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="ad063-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ad063-116">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="ad063-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="ad063-117">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ad063-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad063-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad063-118">Return Value</span></span>

<span data-ttu-id="ad063-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ad063-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad063-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad063-120">Remarks</span></span>

<span data-ttu-id="ad063-121">Para cerrar todos los dispositivos abiertos por la aplicación, especifique el identificador de dispositivo "todos" para el parámetro *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="ad063-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="ad063-122">Al cerrar el dispositivo **cdaudio** se detiene la reproducción de audio.</span><span class="sxs-lookup"><span data-stu-id="ad063-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="ad063-123">**Windows 2000/XP:** Si el dispositivo **cdaudio** se está reproduciendo, el cierre del dispositivo **cdaudio** no hace que el audio deje de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="ad063-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="ad063-124">Envíe primero el comando [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="ad063-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="ad063-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ad063-125">Examples</span></span>

<span data-ttu-id="ad063-126">El siguiente comando cierra el dispositivo "de".</span><span class="sxs-lookup"><span data-stu-id="ad063-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="ad063-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad063-127">Requirements</span></span>



| <span data-ttu-id="ad063-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad063-128">Requirement</span></span> | <span data-ttu-id="ad063-129">Value</span><span class="sxs-lookup"><span data-stu-id="ad063-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad063-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad063-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ad063-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ad063-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad063-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad063-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ad063-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad063-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad063-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad063-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad063-135"><dt>Corecrt \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad063-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad063-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad063-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad063-137">MCI</span><span class="sxs-lookup"><span data-stu-id="ad063-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ad063-138">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="ad063-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

