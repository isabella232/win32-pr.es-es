---
title: comando settimecode
description: El comando settimecode habilita o deshabilita la grabación de código de tiempo para un VCR. Los dispositivos VCR reconocen este comando.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- comando settimecode de Windows multimedia
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804076"
---
# <a name="settimecode-command"></a><span data-ttu-id="acf67-105">comando settimecode</span><span class="sxs-lookup"><span data-stu-id="acf67-105">settimecode command</span></span>

<span data-ttu-id="acf67-106">El comando settimecode habilita o deshabilita la grabación de código de tiempo para un VCR.</span><span class="sxs-lookup"><span data-stu-id="acf67-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="acf67-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="acf67-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="acf67-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="acf67-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="acf67-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acf67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf67-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="acf67-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="acf67-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="acf67-111">Identifier of an MCI device.</span></span> <span data-ttu-id="acf67-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="acf67-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="acf67-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span><span class="sxs-lookup"><span data-stu-id="acf67-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="acf67-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="acf67-114">One of the following flags.</span></span>



| <span data-ttu-id="acf67-115">Value</span><span class="sxs-lookup"><span data-stu-id="acf67-115">Value</span></span>      | <span data-ttu-id="acf67-116">Significado</span><span class="sxs-lookup"><span data-stu-id="acf67-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="acf67-117">grabar en</span><span class="sxs-lookup"><span data-stu-id="acf67-117">record on</span></span>  | <span data-ttu-id="acf67-118">Establece el VCR para grabar el código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="acf67-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="acf67-119">registro desactivado</span><span class="sxs-lookup"><span data-stu-id="acf67-119">record off</span></span> | <span data-ttu-id="acf67-120">Deshabilita la grabación de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="acf67-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="acf67-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="acf67-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="acf67-122">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="acf67-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="acf67-123">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="acf67-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf67-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acf67-124">Return Value</span></span>

<span data-ttu-id="acf67-125">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="acf67-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf67-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acf67-126">Requirements</span></span>



| <span data-ttu-id="acf67-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="acf67-127">Requirement</span></span> | <span data-ttu-id="acf67-128">Value</span><span class="sxs-lookup"><span data-stu-id="acf67-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="acf67-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acf67-129">Minimum supported client</span></span><br/> | <span data-ttu-id="acf67-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="acf67-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="acf67-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acf67-131">Minimum supported server</span></span><br/> | <span data-ttu-id="acf67-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="acf67-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="acf67-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="acf67-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf67-134">MCI</span><span class="sxs-lookup"><span data-stu-id="acf67-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="acf67-135">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="acf67-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

