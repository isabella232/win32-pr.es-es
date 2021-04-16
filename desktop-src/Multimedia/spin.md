---
title: comando de número
description: El comando spin inicia el giro de un disco o detiene el disco. Los dispositivos de videodisco reconocen este comando.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- comando de giro de Windows multimedia
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676797"
---
# <a name="spin-command"></a><span data-ttu-id="d55f4-105">comando de número</span><span class="sxs-lookup"><span data-stu-id="d55f4-105">spin command</span></span>

<span data-ttu-id="d55f4-106">El comando spin inicia el giro de un disco o detiene el disco.</span><span class="sxs-lookup"><span data-stu-id="d55f4-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="d55f4-107">Los dispositivos de videodisco reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="d55f4-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="d55f4-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="d55f4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d55f4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d55f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d55f4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d55f4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d55f4-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d55f4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d55f4-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d55f4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d55f4-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span><span class="sxs-lookup"><span data-stu-id="d55f4-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="d55f4-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="d55f4-114">One of the following flags.</span></span>



| <span data-ttu-id="d55f4-115">Value</span><span class="sxs-lookup"><span data-stu-id="d55f4-115">Value</span></span> | <span data-ttu-id="d55f4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d55f4-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="d55f4-117"> Abajo</span><span class="sxs-lookup"><span data-stu-id="d55f4-117">down</span></span>  | <span data-ttu-id="d55f4-118">Detiene el disco al girar.</span><span class="sxs-lookup"><span data-stu-id="d55f4-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="d55f4-119">up</span><span class="sxs-lookup"><span data-stu-id="d55f4-119">up</span></span>    | <span data-ttu-id="d55f4-120">Inicia la rotación del disco.</span><span class="sxs-lookup"><span data-stu-id="d55f4-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d55f4-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="d55f4-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d55f4-122">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="d55f4-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d55f4-123">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d55f4-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d55f4-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d55f4-124">Return Value</span></span>

<span data-ttu-id="d55f4-125">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d55f4-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="d55f4-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d55f4-126">Examples</span></span>

<span data-ttu-id="d55f4-127">El comando siguiente inicia la rotación de un dispositivo de videodisco.</span><span class="sxs-lookup"><span data-stu-id="d55f4-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="d55f4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d55f4-128">Requirements</span></span>



| <span data-ttu-id="d55f4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d55f4-129">Requirement</span></span> | <span data-ttu-id="d55f4-130">Value</span><span class="sxs-lookup"><span data-stu-id="d55f4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d55f4-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d55f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d55f4-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d55f4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d55f4-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d55f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d55f4-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d55f4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d55f4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d55f4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55f4-136">MCI</span><span class="sxs-lookup"><span data-stu-id="d55f4-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d55f4-137">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d55f4-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

