---
title: Comando MCI_SETTUNER (mmsystem. h)
description: El \_ comando MCI SETTUNER establece el canal actual en el sintonizador. Los dispositivos VCR reconocen este comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Comando de MCI_SETTUNER de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079749"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="f5bef-105">\_Comando MCI SETTUNER</span><span class="sxs-lookup"><span data-stu-id="f5bef-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="f5bef-106">El \_ comando MCI SETTUNER establece el canal actual en el sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f5bef-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="f5bef-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="f5bef-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="f5bef-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5bef-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="f5bef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5bef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5bef-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f5bef-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="f5bef-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f5bef-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="f5bef-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="f5bef-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f5bef-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span><span class="sxs-lookup"><span data-stu-id="f5bef-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-116">Puntero a una estructura de [**\_ \_ \_ parms VCR SETTUNER**](mci-vcr-settuner-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f5bef-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5bef-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5bef-117">Return Value</span></span>

<span data-ttu-id="f5bef-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f5bef-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5bef-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5bef-119">Remarks</span></span>

<span data-ttu-id="f5bef-120">Las siguientes marcas adicionales se aplican a los dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="f5bef-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="f5bef-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_ \_ canal SETTUNER de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f5bef-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-122">El miembro **dwChannel** de la estructura identificada por *lpSetTuner* contiene el nuevo número de canal.</span><span class="sxs-lookup"><span data-stu-id="f5bef-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>canal de SETTUNER de VCR de MCI \_ \_ \_ \_ inactivo</span><span class="sxs-lookup"><span data-stu-id="f5bef-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-124">Disminuye el canal del sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f5bef-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_búsqueda de \_ canal de SETTUNER VCR \_ \_ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f5bef-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-126">Busca un canal válido en la dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="f5bef-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ \_ búsqueda de canal de SETTUNER VCR \_ de MCI</span><span class="sxs-lookup"><span data-stu-id="f5bef-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-128">Busca un canal válido en la dirección de avance.</span><span class="sxs-lookup"><span data-stu-id="f5bef-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_ \_ \_ canal \_ de SETTUNER de VCR de MCI up</span><span class="sxs-lookup"><span data-stu-id="f5bef-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-130">Incrementa el canal del sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f5bef-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="f5bef-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_ \_ número SETTUNER de VCR de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f5bef-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f5bef-132">El miembro **dwNumber** de la estructura identificada por *lpSetTuner* especifica qué sintonizador lógico debe afectar a este comando.</span><span class="sxs-lookup"><span data-stu-id="f5bef-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5bef-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5bef-133">Requirements</span></span>



| <span data-ttu-id="f5bef-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5bef-134">Requirement</span></span> | <span data-ttu-id="f5bef-135">Value</span><span class="sxs-lookup"><span data-stu-id="f5bef-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bef-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5bef-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bef-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5bef-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f5bef-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5bef-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bef-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5bef-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f5bef-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5bef-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5bef-141"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5bef-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bef-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5bef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bef-143">MCI</span><span class="sxs-lookup"><span data-stu-id="f5bef-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f5bef-144">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f5bef-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

