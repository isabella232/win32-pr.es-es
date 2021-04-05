---
title: index (comando)
description: El comando index controla la presentación en pantalla de un VCR. Los dispositivos VCR reconocen este comando.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- comando de índice multimedia de Windows
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997160"
---
# <a name="index-command"></a><span data-ttu-id="7c3d5-105">index (comando)</span><span class="sxs-lookup"><span data-stu-id="7c3d5-105">index command</span></span>

<span data-ttu-id="7c3d5-106">El comando index controla la presentación en pantalla de un VCR.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="7c3d5-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="7c3d5-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7c3d5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c3d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3d5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7c3d5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7c3d5-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="7c3d5-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7c3d5-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span><span class="sxs-lookup"><span data-stu-id="7c3d5-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="7c3d5-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-114">One of the following flags.</span></span>



| <span data-ttu-id="7c3d5-115">Value</span><span class="sxs-lookup"><span data-stu-id="7c3d5-115">Value</span></span> | <span data-ttu-id="7c3d5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7c3d5-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3d5-117">apagado</span><span class="sxs-lookup"><span data-stu-id="7c3d5-117">off</span></span>   | <span data-ttu-id="7c3d5-118">Desactiva la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="7c3d5-119">on</span><span class="sxs-lookup"><span data-stu-id="7c3d5-119">on</span></span>    | <span data-ttu-id="7c3d5-120">Activa la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-120">Turns on the on-screen display.</span></span> <span data-ttu-id="7c3d5-121">El elemento que se va a mostrar se especifica mediante la marca "índice" del comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="7c3d5-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7c3d5-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7c3d5-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7c3d5-123">Puede ser "Wait", "Notify" o "Test".</span><span class="sxs-lookup"><span data-stu-id="7c3d5-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="7c3d5-124">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7c3d5-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3d5-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c3d5-125">Return Value</span></span>

<span data-ttu-id="7c3d5-126">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7c3d5-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3d5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c3d5-127">Requirements</span></span>



| <span data-ttu-id="7c3d5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c3d5-128">Requirement</span></span> | <span data-ttu-id="7c3d5-129">Value</span><span class="sxs-lookup"><span data-stu-id="7c3d5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7c3d5-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c3d5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3d5-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7c3d5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7c3d5-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c3d5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3d5-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c3d5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7c3d5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c3d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3d5-135">MCI</span><span class="sxs-lookup"><span data-stu-id="7c3d5-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7c3d5-136">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="7c3d5-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7c3d5-137">set</span><span class="sxs-lookup"><span data-stu-id="7c3d5-137">set</span></span>](set.md)
</dt> </dl>

 

