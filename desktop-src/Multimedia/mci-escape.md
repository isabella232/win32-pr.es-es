---
title: Comando MCI_ESCAPE (mmsystem. h)
description: El \_ comando MCI escape envía una cadena directamente al dispositivo. Los dispositivos de videodisco reconocen este comando.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- Comando de MCI_ESCAPE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676775"
---
# <a name="mci_escape-command"></a><span data-ttu-id="9dc40-105">Comando de escape de MCI \_</span><span class="sxs-lookup"><span data-stu-id="9dc40-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="9dc40-106">El \_ comando MCI escape envía una cadena directamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dc40-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="9dc40-107">Los dispositivos de videodisco reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="9dc40-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="9dc40-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="9dc40-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="9dc40-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dc40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dc40-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9dc40-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9dc40-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="9dc40-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9dc40-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9dc40-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9dc40-113">\_Notificación de MCI o \_ espera de MCI.</span><span class="sxs-lookup"><span data-stu-id="9dc40-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="9dc40-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9dc40-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dc40-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span><span class="sxs-lookup"><span data-stu-id="9dc40-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="9dc40-116">Puntero a una [**estructura \_ parms de secuencias de \_ escape \_ de MCI Vd**](mci-vd-escape-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9dc40-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dc40-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dc40-117">Return Value</span></span>

<span data-ttu-id="9dc40-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9dc40-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc40-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dc40-119">Remarks</span></span>

<span data-ttu-id="9dc40-120">Los datos que se envían con el escape de MCI \_ dependen del dispositivo y normalmente se pasan directamente al hardware asociado con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dc40-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="9dc40-121">La marca adicional siguiente se aplica a los dispositivos de videodisco:</span><span class="sxs-lookup"><span data-stu-id="9dc40-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="9dc40-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>cadena de escape de MCI \_ Vd \_ \_</span><span class="sxs-lookup"><span data-stu-id="9dc40-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="9dc40-123">Una cadena de comandos se especifica en el miembro **lpstrCommand** de la estructura identificada por *lpEscape*.</span><span class="sxs-lookup"><span data-stu-id="9dc40-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="9dc40-124">Esta marca es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="9dc40-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dc40-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc40-125">Requirements</span></span>



| <span data-ttu-id="9dc40-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc40-126">Requirement</span></span> | <span data-ttu-id="9dc40-127">Value</span><span class="sxs-lookup"><span data-stu-id="9dc40-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc40-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dc40-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc40-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9dc40-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9dc40-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dc40-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc40-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9dc40-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9dc40-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dc40-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dc40-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9dc40-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dc40-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dc40-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc40-135">MCI</span><span class="sxs-lookup"><span data-stu-id="9dc40-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9dc40-136">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="9dc40-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

