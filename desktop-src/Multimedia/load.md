---
title: comando LOAD
description: El comando LOAD carga un archivo en un formato específico del dispositivo. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- comando cargar Windows multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803020"
---
# <a name="load-command"></a><span data-ttu-id="160e3-105">comando LOAD</span><span class="sxs-lookup"><span data-stu-id="160e3-105">load command</span></span>

<span data-ttu-id="160e3-106">El comando LOAD carga un archivo en un formato específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="160e3-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="160e3-107">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="160e3-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="160e3-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="160e3-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="160e3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="160e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="160e3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="160e3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="160e3-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="160e3-111">Identifier of an MCI device.</span></span> <span data-ttu-id="160e3-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="160e3-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="160e3-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span><span class="sxs-lookup"><span data-stu-id="160e3-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="160e3-114">Ruta de acceso y nombre de archivo que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="160e3-114">Path and filename to load.</span></span> <span data-ttu-id="160e3-115">En el caso de los dispositivos de superposición de vídeo, también puede incluir un rectángulo de destino para los datos.</span><span class="sxs-lookup"><span data-stu-id="160e3-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="160e3-116">Para especificar un rectángulo de destino, especifique "at" seguido de **x1 Y1 x2 Y2**, donde **x1 Y1** especifique la esquina superior izquierda del rectángulo y **x2 Y2** especifique el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="160e3-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="160e3-117">El rectángulo es relativo al origen del búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="160e3-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="160e3-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="160e3-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="160e3-119">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="160e3-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="160e3-120">En el caso de los dispositivos de vídeo digital, también se puede especificar "Test".</span><span class="sxs-lookup"><span data-stu-id="160e3-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="160e3-121">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="160e3-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="160e3-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="160e3-122">Return Value</span></span>

<span data-ttu-id="160e3-123">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="160e3-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="160e3-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="160e3-124">Remarks</span></span>

<span data-ttu-id="160e3-125">El dispositivo "vidboard" envía un mensaje de notificación cuando se completa la carga.</span><span class="sxs-lookup"><span data-stu-id="160e3-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="160e3-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="160e3-126">Examples</span></span>

<span data-ttu-id="160e3-127">El comando siguiente carga un archivo en el dispositivo "vidboard".</span><span class="sxs-lookup"><span data-stu-id="160e3-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="160e3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="160e3-128">Requirements</span></span>



| <span data-ttu-id="160e3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="160e3-129">Requirement</span></span> | <span data-ttu-id="160e3-130">Value</span><span class="sxs-lookup"><span data-stu-id="160e3-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="160e3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="160e3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="160e3-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="160e3-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="160e3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="160e3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="160e3-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="160e3-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="160e3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="160e3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="160e3-136">MCI</span><span class="sxs-lookup"><span data-stu-id="160e3-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="160e3-137">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="160e3-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

