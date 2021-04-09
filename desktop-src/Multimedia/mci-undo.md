---
title: Comando MCI_UNDO (mmsystem. h)
description: El \_ comando de deshacer MCI invierte el comando MCI \_ CUT, \_ copia MCI, eliminación de MCI \_ o \_ pegado MCI más reciente. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- Comando de MCI_UNDO de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078985"
---
# <a name="mci_undo-command"></a><span data-ttu-id="82955-105">\_Comando de deshacer MCI</span><span class="sxs-lookup"><span data-stu-id="82955-105">MCI\_UNDO command</span></span>

<span data-ttu-id="82955-106">El \_ comando de deshacer MCI invierte el comando [MCI \_ CUT](mci-cut.md), [ \_ copia MCI](mci-copy.md), [ \_ eliminación](mci-delete.md)de MCI o [ \_ pegado](mci-paste.md) MCI más reciente.</span><span class="sxs-lookup"><span data-stu-id="82955-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="82955-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="82955-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="82955-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="82955-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="82955-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82955-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82955-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="82955-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="82955-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="82955-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="82955-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="82955-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="82955-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="82955-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="82955-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="82955-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="82955-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span><span class="sxs-lookup"><span data-stu-id="82955-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="82955-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="82955-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="82955-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="82955-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82955-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82955-118">Return Value</span></span>

<span data-ttu-id="82955-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="82955-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="82955-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82955-120">Requirements</span></span>



| <span data-ttu-id="82955-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="82955-121">Requirement</span></span> | <span data-ttu-id="82955-122">Value</span><span class="sxs-lookup"><span data-stu-id="82955-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82955-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82955-123">Minimum supported client</span></span><br/> | <span data-ttu-id="82955-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82955-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="82955-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82955-125">Minimum supported server</span></span><br/> | <span data-ttu-id="82955-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82955-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="82955-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82955-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="82955-128"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82955-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82955-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="82955-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82955-130">MCI</span><span class="sxs-lookup"><span data-stu-id="82955-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="82955-131">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="82955-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

