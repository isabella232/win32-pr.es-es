---
title: Comando MCI_SPIN (mmsystem. h)
description: El \_ comando MCI spin inicia el dispositivo que gira hacia arriba o hacia abajo. Los dispositivos de videodisco reconocen este comando.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- Comando de MCI_SPIN de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422221"
---
# <a name="mci_spin-command"></a><span data-ttu-id="39826-105">Comando de giro de MCI \_</span><span class="sxs-lookup"><span data-stu-id="39826-105">MCI\_SPIN command</span></span>

<span data-ttu-id="39826-106">El \_ comando MCI spin inicia el dispositivo que gira hacia arriba o hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="39826-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="39826-107">Los dispositivos de videodisco reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="39826-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="39826-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="39826-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="39826-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39826-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39826-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="39826-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="39826-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="39826-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="39826-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="39826-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="39826-113">\_Notificación de MCI o \_ espera de MCI.</span><span class="sxs-lookup"><span data-stu-id="39826-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="39826-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="39826-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="39826-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span><span class="sxs-lookup"><span data-stu-id="39826-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="39826-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="39826-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="39826-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="39826-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39826-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39826-118">Return Value</span></span>

<span data-ttu-id="39826-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="39826-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39826-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39826-120">Remarks</span></span>

<span data-ttu-id="39826-121">Las siguientes marcas adicionales se aplican a los dispositivos de VideoDisc:</span><span class="sxs-lookup"><span data-stu-id="39826-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="39826-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>Desactivación de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="39826-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="39826-123">Detiene el giro del disco.</span><span class="sxs-lookup"><span data-stu-id="39826-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="39826-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>arranque \_ de MCI Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="39826-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="39826-125">Inicia el giro del disco.</span><span class="sxs-lookup"><span data-stu-id="39826-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39826-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39826-126">Requirements</span></span>



| <span data-ttu-id="39826-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="39826-127">Requirement</span></span> | <span data-ttu-id="39826-128">Value</span><span class="sxs-lookup"><span data-stu-id="39826-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39826-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39826-129">Minimum supported client</span></span><br/> | <span data-ttu-id="39826-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39826-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="39826-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39826-131">Minimum supported server</span></span><br/> | <span data-ttu-id="39826-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39826-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="39826-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39826-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="39826-134"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39826-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39826-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="39826-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39826-136">MCI</span><span class="sxs-lookup"><span data-stu-id="39826-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="39826-137">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="39826-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

