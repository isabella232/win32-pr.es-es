---
title: comando de realización
description: El comando de vista indica a un dispositivo que seleccione y dé su paleta en el contexto de presentación de la ventana mostrada. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- obtener comandos de Windows multimedia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996952"
---
# <a name="realize-command"></a><span data-ttu-id="5bf14-105">comando de realización</span><span class="sxs-lookup"><span data-stu-id="5bf14-105">realize command</span></span>

<span data-ttu-id="5bf14-106">El comando de vista indica a un dispositivo que seleccione y dé su paleta en el contexto de presentación de la ventana mostrada.</span><span class="sxs-lookup"><span data-stu-id="5bf14-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="5bf14-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="5bf14-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="5bf14-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="5bf14-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5bf14-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bf14-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf14-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="5bf14-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5bf14-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="5bf14-111">Identifier of an MCI device.</span></span> <span data-ttu-id="5bf14-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bf14-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5bf14-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span><span class="sxs-lookup"><span data-stu-id="5bf14-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="5bf14-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="5bf14-114">One of the following flags.</span></span>



| <span data-ttu-id="5bf14-115">Value</span><span class="sxs-lookup"><span data-stu-id="5bf14-115">Value</span></span>      | <span data-ttu-id="5bf14-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5bf14-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="5bf14-117">background</span><span class="sxs-lookup"><span data-stu-id="5bf14-117">background</span></span> | <span data-ttu-id="5bf14-118">Obtiene la paleta como una paleta de fondo.</span><span class="sxs-lookup"><span data-stu-id="5bf14-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="5bf14-119">normal</span><span class="sxs-lookup"><span data-stu-id="5bf14-119">normal</span></span>     | <span data-ttu-id="5bf14-120">Obtiene la paleta de una ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="5bf14-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="5bf14-121">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5bf14-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5bf14-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="5bf14-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5bf14-123">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="5bf14-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="5bf14-124">En el caso de los dispositivos de vídeo digital, también se puede especificar "Test".</span><span class="sxs-lookup"><span data-stu-id="5bf14-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="5bf14-125">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5bf14-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf14-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bf14-126">Return Value</span></span>

<span data-ttu-id="5bf14-127">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5bf14-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf14-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bf14-128">Remarks</span></span>

<span data-ttu-id="5bf14-129">Use este comando solo si la aplicación usa un identificador de ventana y recibe un mensaje de **WM \_ QUERYNEWPALLETTE** o **WM \_ PALETTECHANGED** .</span><span class="sxs-lookup"><span data-stu-id="5bf14-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="5bf14-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5bf14-130">Examples</span></span>

<span data-ttu-id="5bf14-131">El comando siguiente indica al dispositivo "Televideo" que dé su paleta.</span><span class="sxs-lookup"><span data-stu-id="5bf14-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="5bf14-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bf14-132">Requirements</span></span>



| <span data-ttu-id="5bf14-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf14-133">Requirement</span></span> | <span data-ttu-id="5bf14-134">Value</span><span class="sxs-lookup"><span data-stu-id="5bf14-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5bf14-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bf14-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf14-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5bf14-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5bf14-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bf14-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf14-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bf14-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5bf14-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bf14-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf14-140">MCI</span><span class="sxs-lookup"><span data-stu-id="5bf14-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5bf14-141">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="5bf14-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

