---
title: Comando MCI_REALIZE (mmsystem. h)
description: El \_ comando MCI Observate hace que un dispositivo gráfico obtenga su paleta en un contexto de dispositivo (DC). Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Comando de MCI_REALIZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651394"
---
# <a name="mci_realize-command"></a><span data-ttu-id="8df8e-105">Comando de MCI \_</span><span class="sxs-lookup"><span data-stu-id="8df8e-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="8df8e-106">El \_ comando MCI Observate hace que un dispositivo gráfico obtenga su paleta en un contexto de dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="8df8e-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="8df8e-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="8df8e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8df8e-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="8df8e-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="8df8e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8df8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df8e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8df8e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="8df8e-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8df8e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-113">**MCI \_ NOTIFICAr**, **\_ espera de MCI** o, para dispositivos de vídeo digital **, \_ prueba de MCI**.</span><span class="sxs-lookup"><span data-stu-id="8df8e-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="8df8e-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8df8e-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span><span class="sxs-lookup"><span data-stu-id="8df8e-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8df8e-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8df8e-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="8df8e-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df8e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8df8e-118">Return Value</span></span>

<span data-ttu-id="8df8e-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8df8e-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df8e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8df8e-120">Remarks</span></span>

<span data-ttu-id="8df8e-121">Debe usar este comando cuando la aplicación reciba el mensaje [**de \_ QUERYNEWPALETTE de WM**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="8df8e-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="8df8e-122">Se usan las siguientes marcas adicionales con el tipo de dispositivo "DigitalVideo":</span><span class="sxs-lookup"><span data-stu-id="8df8e-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="8df8e-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ obtener \_ BKGD</span><span class="sxs-lookup"><span data-stu-id="8df8e-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-124">Obtiene la paleta como una paleta de fondo.</span><span class="sxs-lookup"><span data-stu-id="8df8e-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="8df8e-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>\_norma de DGV de MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="8df8e-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="8df8e-126">Obtiene la paleta normalmente.</span><span class="sxs-lookup"><span data-stu-id="8df8e-126">Realizes the palette normally.</span></span> <span data-ttu-id="8df8e-127">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8df8e-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="8df8e-128">En el caso de los dispositivos de vídeo digital, el parámetro *lpRealize* apunta a una estructura de **MCI \_ \_ parms** .</span><span class="sxs-lookup"><span data-stu-id="8df8e-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="8df8e-129">Para obtener más información, consulte comentarios en la estructura [**\_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8df8e-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df8e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8df8e-130">Requirements</span></span>



| <span data-ttu-id="8df8e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df8e-131">Requirement</span></span> | <span data-ttu-id="8df8e-132">Value</span><span class="sxs-lookup"><span data-stu-id="8df8e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df8e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8df8e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8df8e-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8df8e-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8df8e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8df8e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8df8e-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8df8e-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8df8e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8df8e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df8e-138"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8df8e-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df8e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8df8e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df8e-140">MCI</span><span class="sxs-lookup"><span data-stu-id="8df8e-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8df8e-141">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="8df8e-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

