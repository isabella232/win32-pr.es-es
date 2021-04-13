---
title: Comando MCI_CONFIGURE (mmsystem. h)
description: El \_ comando MCI configure muestra un cuadro de diálogo para establecer las opciones de funcionamiento. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- Comando de MCI_CONFIGURE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421975"
---
# <a name="mci_configure-command"></a><span data-ttu-id="0576b-105">Comando de configuración de MCI \_</span><span class="sxs-lookup"><span data-stu-id="0576b-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="0576b-106">El \_ comando MCI configure muestra un cuadro de diálogo para establecer las opciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="0576b-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="0576b-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="0576b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="0576b-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="0576b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="0576b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0576b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0576b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0576b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0576b-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="0576b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="0576b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="0576b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0576b-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="0576b-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="0576b-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0576b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0576b-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span><span class="sxs-lookup"><span data-stu-id="0576b-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="0576b-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0576b-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="0576b-117">(Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="0576b-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0576b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0576b-118">Return Value</span></span>

<span data-ttu-id="0576b-119">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0576b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0576b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0576b-120">Requirements</span></span>



| <span data-ttu-id="0576b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0576b-121">Requirement</span></span> | <span data-ttu-id="0576b-122">Value</span><span class="sxs-lookup"><span data-stu-id="0576b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0576b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0576b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0576b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0576b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0576b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0576b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0576b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0576b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0576b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0576b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0576b-128"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0576b-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0576b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0576b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0576b-130">MCI</span><span class="sxs-lookup"><span data-stu-id="0576b-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0576b-131">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="0576b-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

