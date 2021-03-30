---
title: comando configurar
description: El comando configurar muestra un cuadro de diálogo que se usa para configurar el dispositivo. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- configurar comandos de Windows multimedia
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801028"
---
# <a name="configure-command"></a><span data-ttu-id="0c0ea-105">comando configurar</span><span class="sxs-lookup"><span data-stu-id="0c0ea-105">configure command</span></span>

<span data-ttu-id="0c0ea-106">El comando configurar muestra un cuadro de diálogo que se usa para configurar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c0ea-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="0c0ea-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="0c0ea-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="0c0ea-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c0ea-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0c0ea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c0ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c0ea-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0c0ea-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0c0ea-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0c0ea-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0c0ea-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c0ea-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0c0ea-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0c0ea-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0c0ea-114">Puede ser "Wait", "Notify" o "Test".</span><span class="sxs-lookup"><span data-stu-id="0c0ea-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="0c0ea-115">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0c0ea-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c0ea-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c0ea-116">Return Value</span></span>

<span data-ttu-id="0c0ea-117">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0c0ea-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c0ea-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c0ea-118">Requirements</span></span>



| <span data-ttu-id="0c0ea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c0ea-119">Requirement</span></span> | <span data-ttu-id="0c0ea-120">Value</span><span class="sxs-lookup"><span data-stu-id="0c0ea-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0c0ea-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c0ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0ea-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c0ea-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c0ea-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c0ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0ea-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c0ea-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0c0ea-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c0ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0ea-126">MCI</span><span class="sxs-lookup"><span data-stu-id="0c0ea-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0c0ea-127">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="0c0ea-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

