---
title: Comando MCI_MONITOR (mmsystem. h)
description: El \_ comando MCI monitor especifica el origen de la presentación. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- Comando de MCI_MONITOR de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996700"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="d2fd1-105">Comando de monitor de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d2fd1-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="d2fd1-106">El \_ comando MCI monitor especifica el origen de la presentación.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="d2fd1-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d2fd1-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="d2fd1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2fd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2fd1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d2fd1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d2fd1-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d2fd1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d2fd1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d2fd1-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d2fd1-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d2fd1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2fd1-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span><span class="sxs-lookup"><span data-stu-id="d2fd1-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="d2fd1-116">Puntero a una estructura de [**\_ DGV \_ monitor \_ parms de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .</span><span class="sxs-lookup"><span data-stu-id="d2fd1-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2fd1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2fd1-117">Return Value</span></span>

<span data-ttu-id="d2fd1-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2fd1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2fd1-119">Remarks</span></span>

<span data-ttu-id="d2fd1-120">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="d2fd1-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="d2fd1-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI \_ DGV \_ monitor ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="d2fd1-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="d2fd1-122">Una constante que indica que el método de supervisión se incluye en el miembro **dwMethod** de la estructura identificada por *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="d2fd1-123">Cuando \_ \_ se usa la marca de entrada del monitor MCI DGV \_ en el miembro **dwSource** , se selecciona el método de supervisión.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="d2fd1-124">Normalmente, los distintos métodos de supervisión tienen implicaciones diferentes en la forma en que se usa el hardware.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="d2fd1-125">El dispositivo selecciona el método de supervisión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="d2fd1-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_origen del \_ monitor MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="d2fd1-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="d2fd1-127">Una constante que indica que el origen del monitor se incluye en el miembro **dwSource** de la estructura identificada por *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="d2fd1-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2fd1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2fd1-128">Requirements</span></span>



| <span data-ttu-id="d2fd1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2fd1-129">Requirement</span></span> | <span data-ttu-id="d2fd1-130">Value</span><span class="sxs-lookup"><span data-stu-id="d2fd1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fd1-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2fd1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d2fd1-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2fd1-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d2fd1-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2fd1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d2fd1-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2fd1-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d2fd1-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2fd1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2fd1-136"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2fd1-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2fd1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2fd1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2fd1-138">MCI</span><span class="sxs-lookup"><span data-stu-id="d2fd1-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d2fd1-139">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d2fd1-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

