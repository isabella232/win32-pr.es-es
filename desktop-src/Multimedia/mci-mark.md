---
title: Comando MCI_MARK (mmsystem. h)
description: El \_ comando de marca MCI registra o borra marcas que se pueden usar con el \_ comando MCI Seek para búsquedas de alta velocidad. Los dispositivos VCR reconocen este comando.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- Comando de MCI_MARK de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079063"
---
# <a name="mci_mark-command"></a><span data-ttu-id="27784-105">\_Comando de marca MCI</span><span class="sxs-lookup"><span data-stu-id="27784-105">MCI\_MARK command</span></span>

<span data-ttu-id="27784-106">El \_ comando de marca MCI registra o borra marcas que se pueden usar con el comando [MCI \_ Seek](mci-seek.md) para búsquedas de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="27784-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="27784-107">Los dispositivos VCR reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="27784-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="27784-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="27784-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="27784-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27784-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27784-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="27784-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="27784-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="27784-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="27784-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="27784-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="27784-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="27784-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="27784-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="27784-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="27784-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span><span class="sxs-lookup"><span data-stu-id="27784-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="27784-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="27784-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="27784-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="27784-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27784-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27784-118">Return Value</span></span>

<span data-ttu-id="27784-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="27784-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="27784-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27784-120">Remarks</span></span>

<span data-ttu-id="27784-121">Las siguientes marcas adicionales se aplican a los dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="27784-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="27784-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_borrado de la marca de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="27784-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="27784-123">Borra una marca en la posición actual si existe una.</span><span class="sxs-lookup"><span data-stu-id="27784-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="27784-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_escritura de \_ marca de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="27784-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="27784-125">Escribe una marca en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="27784-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27784-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27784-126">Requirements</span></span>



| <span data-ttu-id="27784-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="27784-127">Requirement</span></span> | <span data-ttu-id="27784-128">Value</span><span class="sxs-lookup"><span data-stu-id="27784-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27784-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27784-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27784-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="27784-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27784-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27784-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27784-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27784-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27784-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27784-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="27784-134"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27784-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27784-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="27784-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27784-136">MCI</span><span class="sxs-lookup"><span data-stu-id="27784-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="27784-137">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="27784-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

