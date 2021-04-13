---
title: Break (comando)
description: El comando break especifica una clave para anular un comando que se invocó mediante \ 0034; wait \ 0034; marcas. Este comando es un comando del sistema MCI; lo interpreta directamente MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando interrumpir Windows multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492826"
---
# <a name="break-command"></a><span data-ttu-id="2bb07-105">Break (comando)</span><span class="sxs-lookup"><span data-stu-id="2bb07-105">break command</span></span>

<span data-ttu-id="2bb07-106">El comando break especifica una clave para anular un comando que se invocó mediante la marca "Wait".</span><span class="sxs-lookup"><span data-stu-id="2bb07-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="2bb07-107">Este comando es un comando del sistema MCI; lo interpreta directamente MCI.</span><span class="sxs-lookup"><span data-stu-id="2bb07-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="2bb07-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2bb07-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="2bb07-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bb07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb07-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2bb07-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2bb07-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="2bb07-111">Identifier of an MCI device.</span></span> <span data-ttu-id="2bb07-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bb07-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="2bb07-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span><span class="sxs-lookup"><span data-stu-id="2bb07-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="2bb07-114">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2bb07-114">One of the following flags.</span></span>



| <span data-ttu-id="2bb07-115">Value</span><span class="sxs-lookup"><span data-stu-id="2bb07-115">Value</span></span>                 | <span data-ttu-id="2bb07-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2bb07-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2bb07-117">en *código de tecla virtual*</span><span class="sxs-lookup"><span data-stu-id="2bb07-117">on *virtual key code*</span></span> | <span data-ttu-id="2bb07-118">Especifica la clave que anula un comando que se inició con la marca "Wait".</span><span class="sxs-lookup"><span data-stu-id="2bb07-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="2bb07-119">apagado</span><span class="sxs-lookup"><span data-stu-id="2bb07-119">off</span></span>                   | <span data-ttu-id="2bb07-120">Deshabilita la clave de interrupción actual.</span><span class="sxs-lookup"><span data-stu-id="2bb07-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="2bb07-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="2bb07-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2bb07-122">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="2bb07-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="2bb07-123">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="2bb07-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="2bb07-124">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2bb07-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bb07-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bb07-125">Return Value</span></span>

<span data-ttu-id="2bb07-126">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2bb07-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb07-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bb07-127">Remarks</span></span>

<span data-ttu-id="2bb07-128">Cuando la tecla interrumpir está habilitada y el usuario presiona la clave identificada por el código de clave virtual especificado en el parámetro *lpszVirtKey* , el dispositivo devuelve el control a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bb07-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="2bb07-129">Si es posible, el comando continúa la ejecución.</span><span class="sxs-lookup"><span data-stu-id="2bb07-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="2bb07-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2bb07-130">Examples</span></span>

<span data-ttu-id="2bb07-131">El siguiente comando establece F2 como tecla de interrupción para el dispositivo "de".</span><span class="sxs-lookup"><span data-stu-id="2bb07-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="2bb07-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bb07-132">Requirements</span></span>



| <span data-ttu-id="2bb07-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bb07-133">Requirement</span></span> | <span data-ttu-id="2bb07-134">Value</span><span class="sxs-lookup"><span data-stu-id="2bb07-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bb07-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb07-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb07-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2bb07-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2bb07-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb07-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb07-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bb07-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2bb07-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bb07-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb07-140">MCI</span><span class="sxs-lookup"><span data-stu-id="2bb07-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2bb07-141">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="2bb07-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

