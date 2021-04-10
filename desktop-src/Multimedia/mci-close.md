---
title: Comando MCI_CLOSE (mmsystem. h)
description: El \_ comando MCI Close libera el acceso a un dispositivo o archivo. Todos los dispositivos reconocen este comando.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- Comando de MCI_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150175"
---
# <a name="mci_close-command"></a><span data-ttu-id="7e694-105">Comando de cierre de MCI \_</span><span class="sxs-lookup"><span data-stu-id="7e694-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="7e694-106">El \_ comando MCI Close libera el acceso a un dispositivo o archivo.</span><span class="sxs-lookup"><span data-stu-id="7e694-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="7e694-107">Todos los dispositivos reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="7e694-107">All devices recognize this command.</span></span>

<span data-ttu-id="7e694-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e694-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="7e694-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e694-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e694-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7e694-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7e694-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="7e694-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7e694-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7e694-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7e694-113">\_Notificación de MCI o \_ espera de MCI.</span><span class="sxs-lookup"><span data-stu-id="7e694-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="7e694-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7e694-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e694-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span><span class="sxs-lookup"><span data-stu-id="7e694-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="7e694-116">Puntero a una [**estructura \_ \_ parms genérica de MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7e694-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="7e694-117">(También puede usar una estructura **\_ \_ parms de cierre de MCI** .</span><span class="sxs-lookup"><span data-stu-id="7e694-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="7e694-118">Para obtener más información, vea los comentarios de **MCI \_ Generic \_ parms**).</span><span class="sxs-lookup"><span data-stu-id="7e694-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e694-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e694-119">Return Value</span></span>

<span data-ttu-id="7e694-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7e694-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e694-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e694-121">Remarks</span></span>

<span data-ttu-id="7e694-122">Salir de una aplicación sin cerrar los dispositivos MCI abiertos puede dejar el dispositivo inaccesible.</span><span class="sxs-lookup"><span data-stu-id="7e694-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="7e694-123">La aplicación debe cerrar explícitamente cada dispositivo o archivo cuando termine de usarlo.</span><span class="sxs-lookup"><span data-stu-id="7e694-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="7e694-124">MCI descarga el dispositivo cuando se cierran todas las instancias del dispositivo o todos los archivos asociados.</span><span class="sxs-lookup"><span data-stu-id="7e694-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e694-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e694-125">Requirements</span></span>



| <span data-ttu-id="7e694-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e694-126">Requirement</span></span> | <span data-ttu-id="7e694-127">Value</span><span class="sxs-lookup"><span data-stu-id="7e694-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e694-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e694-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e694-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7e694-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7e694-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e694-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e694-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e694-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7e694-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e694-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e694-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e694-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e694-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e694-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e694-135">MCI</span><span class="sxs-lookup"><span data-stu-id="7e694-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7e694-136">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="7e694-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

