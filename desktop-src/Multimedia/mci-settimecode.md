---
title: Comando MCI_SETTIMECODE (mmsystem. h)
description: El \_ comando MCI SETTIMECODE habilita o deshabilita la grabación de código de tiempo para un VCR. Los dispositivos VCR reconocen este comando.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- Comando de MCI_SETTIMECODE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676983"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="e671d-105">\_Comando MCI SETTIMECODE</span><span class="sxs-lookup"><span data-stu-id="e671d-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="e671d-106">El \_ comando MCI SETTIMECODE habilita o deshabilita la grabación de código de tiempo para un VCR.</span><span class="sxs-lookup"><span data-stu-id="e671d-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="e671d-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="e671d-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="e671d-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="e671d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="e671d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e671d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e671d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e671d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e671d-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="e671d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="e671d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e671d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e671d-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="e671d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="e671d-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e671d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e671d-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span><span class="sxs-lookup"><span data-stu-id="e671d-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="e671d-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e671d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="e671d-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="e671d-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e671d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e671d-118">Return Value</span></span>

<span data-ttu-id="e671d-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e671d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e671d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e671d-120">Remarks</span></span>

<span data-ttu-id="e671d-121">La marca adicional siguiente se aplica a los dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="e671d-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="e671d-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_registro de \_ SETTIMECODE de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="e671d-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="e671d-123">Establece la grabación de seguimiento de código de tiempo en activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="e671d-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="e671d-124">Esta marca se usa en combinación con una de las siguientes marcas adicionales:</span><span class="sxs-lookup"><span data-stu-id="e671d-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="e671d-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activado \_</span><span class="sxs-lookup"><span data-stu-id="e671d-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="e671d-126">Grabación de código de tiempo activada.</span><span class="sxs-lookup"><span data-stu-id="e671d-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="e671d-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>Desactivación de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="e671d-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="e671d-128">Grabación de código de tiempo desactivada.</span><span class="sxs-lookup"><span data-stu-id="e671d-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e671d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e671d-129">Requirements</span></span>



| <span data-ttu-id="e671d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e671d-130">Requirement</span></span> | <span data-ttu-id="e671d-131">Value</span><span class="sxs-lookup"><span data-stu-id="e671d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e671d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e671d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e671d-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e671d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e671d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e671d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e671d-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e671d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e671d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e671d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e671d-137"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e671d-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e671d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e671d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e671d-139">MCI</span><span class="sxs-lookup"><span data-stu-id="e671d-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e671d-140">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="e671d-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

