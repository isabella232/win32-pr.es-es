---
title: Undo (comando)
description: El comando Deshacer invierte la acción realizada por el comando Copiar, cortar, eliminar, deshacer o pegar más reciente. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- comando Deshacer de Windows multimedia
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079737"
---
# <a name="undo-command"></a><span data-ttu-id="44258-105">Undo (comando)</span><span class="sxs-lookup"><span data-stu-id="44258-105">undo command</span></span>

<span data-ttu-id="44258-106">El comando Deshacer invierte la acción realizada por el comando [copiar](copy.md), [cortar](cut.md), [eliminar](delete.md), deshacer o [pegar](paste.md) más reciente.</span><span class="sxs-lookup"><span data-stu-id="44258-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="44258-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="44258-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="44258-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="44258-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="44258-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44258-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44258-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="44258-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="44258-111">Identificador de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="44258-111">Identifier of an MCI device.</span></span> <span data-ttu-id="44258-112">Este identificador o alias se asigna cuando se abre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44258-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="44258-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="44258-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="44258-114">Puede ser "Wait", "Notify", "Test" o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="44258-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="44258-115">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="44258-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44258-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44258-116">Return Value</span></span>

<span data-ttu-id="44258-117">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="44258-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="44258-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44258-118">Requirements</span></span>



| <span data-ttu-id="44258-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44258-119">Requirement</span></span> | <span data-ttu-id="44258-120">Value</span><span class="sxs-lookup"><span data-stu-id="44258-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="44258-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44258-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44258-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="44258-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="44258-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44258-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44258-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44258-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="44258-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="44258-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44258-126">MCI</span><span class="sxs-lookup"><span data-stu-id="44258-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="44258-127">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="44258-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="44258-128">copy</span><span class="sxs-lookup"><span data-stu-id="44258-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="44258-129">límite</span><span class="sxs-lookup"><span data-stu-id="44258-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="44258-130">delete</span><span class="sxs-lookup"><span data-stu-id="44258-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="44258-131">copiar</span><span class="sxs-lookup"><span data-stu-id="44258-131">paste</span></span>](paste.md)
</dt> </dl>

 

