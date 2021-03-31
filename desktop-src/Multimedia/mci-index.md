---
title: Comando MCI_INDEX (mmsystem. h)
description: El \_ comando MCI index activa o desactiva la presentación en pantalla. Los dispositivos VCR reconocen este comando.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- Comando de MCI_INDEX de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151127"
---
# <a name="mci_index-command"></a><span data-ttu-id="98583-105">\_Comando MCI index</span><span class="sxs-lookup"><span data-stu-id="98583-105">MCI\_INDEX command</span></span>

<span data-ttu-id="98583-106">El \_ comando MCI index activa o desactiva la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="98583-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="98583-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="98583-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="98583-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="98583-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="98583-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98583-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98583-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="98583-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="98583-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="98583-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="98583-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="98583-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="98583-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="98583-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="98583-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="98583-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="98583-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span><span class="sxs-lookup"><span data-stu-id="98583-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="98583-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="98583-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="98583-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="98583-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98583-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98583-118">Return Value</span></span>

<span data-ttu-id="98583-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98583-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98583-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98583-120">Remarks</span></span>

<span data-ttu-id="98583-121">La información que se presenta en la pantalla se controla mediante la marca de \_ Índice del conjunto de VCR \_ de MCI \_ en el comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="98583-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="98583-122">Las siguientes marcas adicionales se aplican a los dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="98583-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="98583-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="98583-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="98583-124">Desactiva la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="98583-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="98583-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="98583-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="98583-126">Activa la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="98583-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98583-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98583-127">Requirements</span></span>



| <span data-ttu-id="98583-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="98583-128">Requirement</span></span> | <span data-ttu-id="98583-129">Value</span><span class="sxs-lookup"><span data-stu-id="98583-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98583-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98583-130">Minimum supported client</span></span><br/> | <span data-ttu-id="98583-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98583-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98583-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98583-132">Minimum supported server</span></span><br/> | <span data-ttu-id="98583-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98583-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98583-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98583-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="98583-135"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98583-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98583-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="98583-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98583-137">MCI</span><span class="sxs-lookup"><span data-stu-id="98583-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="98583-138">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="98583-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

