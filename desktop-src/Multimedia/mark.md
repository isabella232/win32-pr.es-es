---
title: marcar comando
description: El comando marcar controla la grabación y el borrado de marcas en la cinta de vídeo. Los dispositivos VCR reconocen este comando.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- comando marcar Windows multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676719"
---
# <a name="mark-command"></a><span data-ttu-id="9ede6-105">marcar comando</span><span class="sxs-lookup"><span data-stu-id="9ede6-105">mark command</span></span>

<span data-ttu-id="9ede6-106">El comando marcar controla la grabación y el borrado de marcas en la cinta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9ede6-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="9ede6-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="9ede6-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="9ede6-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9ede6-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9ede6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ede6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ede6-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9ede6-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9ede6-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="9ede6-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9ede6-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ede6-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9ede6-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span><span class="sxs-lookup"><span data-stu-id="9ede6-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="9ede6-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ede6-114">One of the following flags.</span></span>



| <span data-ttu-id="9ede6-115">Value</span><span class="sxs-lookup"><span data-stu-id="9ede6-115">Value</span></span> | <span data-ttu-id="9ede6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9ede6-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ede6-117">erase</span><span class="sxs-lookup"><span data-stu-id="9ede6-117">erase</span></span> | <span data-ttu-id="9ede6-118">Borra una marca en la posición actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="9ede6-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="9ede6-119">Para borrar una marca, primero busque la marca y, a continuación, emita el comando marcar "borrar".</span><span class="sxs-lookup"><span data-stu-id="9ede6-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="9ede6-120">escritura</span><span class="sxs-lookup"><span data-stu-id="9ede6-120">write</span></span> | <span data-ttu-id="9ede6-121">Escribe una marca en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="9ede6-121">Writes a mark at the current position.</span></span> <span data-ttu-id="9ede6-122">Es posible que el VCR tenga que estar en modo de reproducción o grabación para que este comando se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ede6-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="9ede6-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="9ede6-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9ede6-124">Puede ser "Wait", "Notify" o "Test".</span><span class="sxs-lookup"><span data-stu-id="9ede6-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="9ede6-125">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9ede6-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ede6-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ede6-126">Return Value</span></span>

<span data-ttu-id="9ede6-127">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9ede6-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ede6-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ede6-128">Remarks</span></span>

<span data-ttu-id="9ede6-129">Las marcas son señales especiales escritas en el contenido que el VCR puede detectar durante las búsquedas de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="9ede6-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="9ede6-130">Las marcas son específicas del VCR.</span><span class="sxs-lookup"><span data-stu-id="9ede6-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ede6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ede6-131">Requirements</span></span>



| <span data-ttu-id="9ede6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ede6-132">Requirement</span></span> | <span data-ttu-id="9ede6-133">Value</span><span class="sxs-lookup"><span data-stu-id="9ede6-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9ede6-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ede6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9ede6-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ede6-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ede6-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ede6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9ede6-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ede6-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9ede6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ede6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ede6-139">MCI</span><span class="sxs-lookup"><span data-stu-id="9ede6-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9ede6-140">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="9ede6-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

