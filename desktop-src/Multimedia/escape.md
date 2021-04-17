---
title: escape (comando)
description: El comando escape envía información específica del dispositivo a un dispositivo. Los dispositivos de videodisco reconocen este comando.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- comando de escape de Windows multimedia
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651384"
---
# <a name="escape-command"></a><span data-ttu-id="89d12-105">escape (comando)</span><span class="sxs-lookup"><span data-stu-id="89d12-105">escape command</span></span>

<span data-ttu-id="89d12-106">El comando escape envía información específica del dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89d12-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="89d12-107">Los dispositivos de videodisco reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="89d12-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="89d12-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="89d12-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="89d12-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89d12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d12-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="89d12-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="89d12-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="89d12-111">Identifier of an MCI device.</span></span> <span data-ttu-id="89d12-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89d12-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="89d12-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span><span class="sxs-lookup"><span data-stu-id="89d12-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="89d12-114">Información personalizada que se va a enviar al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89d12-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="89d12-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="89d12-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="89d12-116">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="89d12-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="89d12-117">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="89d12-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d12-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89d12-118">Return Value</span></span>

<span data-ttu-id="89d12-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="89d12-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="89d12-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="89d12-120">Examples</span></span>

<span data-ttu-id="89d12-121">El comando siguiente envía la cadena de escape "SA" al dispositivo de VideoDisc.</span><span class="sxs-lookup"><span data-stu-id="89d12-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="89d12-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d12-122">Requirements</span></span>



| <span data-ttu-id="89d12-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d12-123">Requirement</span></span> | <span data-ttu-id="89d12-124">Value</span><span class="sxs-lookup"><span data-stu-id="89d12-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="89d12-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89d12-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89d12-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="89d12-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89d12-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89d12-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89d12-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89d12-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="89d12-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="89d12-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d12-130">MCI</span><span class="sxs-lookup"><span data-stu-id="89d12-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="89d12-131">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="89d12-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

