---
title: Comando MCI_LOAD (mmsystem. h)
description: El comando de carga de MCI \_ carga un archivo. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Comando de MCI_LOAD de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995917"
---
# <a name="mci_load-command"></a><span data-ttu-id="d7654-105">\_Comando carga de MCI</span><span class="sxs-lookup"><span data-stu-id="d7654-105">MCI\_LOAD command</span></span>

<span data-ttu-id="d7654-106">El comando de carga de MCI \_ carga un archivo.</span><span class="sxs-lookup"><span data-stu-id="d7654-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="d7654-107">Los dispositivos de vídeo digital y de superposición reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="d7654-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="d7654-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7654-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="d7654-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7654-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7654-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d7654-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d7654-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="d7654-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d7654-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d7654-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d7654-113">\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d7654-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="d7654-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d7654-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7654-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span><span class="sxs-lookup"><span data-stu-id="d7654-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="d7654-116">Puntero a una [**estructura \_ \_ parms de carga de MCI**](mci-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d7654-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="d7654-117">(Los dispositivos con parámetros adicionales podrían reemplazar esta estructura con una estructura específica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7654-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="d7654-118">En el caso de los dispositivos de vídeo digital, el parámetro **lpLoad** apunta a una estructura [**DGV de \_ \_ carga \_ parms de MCI**](/previous-versions//dd743391(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d7654-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7654-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7654-119">Return Value</span></span>

<span data-ttu-id="d7654-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d7654-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7654-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7654-121">Remarks</span></span>

<span data-ttu-id="d7654-122">La marca adicional siguiente se aplica a todos los dispositivos que admiten la carga de MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="d7654-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="d7654-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_archivo de carga de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d7654-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="d7654-124">El miembro **lpfilename** de la estructura identificada por *lpLoad* contiene una dirección de un búfer que contiene el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d7654-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="d7654-125">La siguiente marca adicional se usa con el tipo de dispositivo **superpuesto** :</span><span class="sxs-lookup"><span data-stu-id="d7654-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d7654-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="d7654-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="d7654-127">El miembro **RC** de la estructura identificada por *lpLoad* contiene un rectángulo de presentación válido que identifica el área del búfer de vídeo que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="d7654-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="d7654-128">En el caso de los dispositivos de superposición de vídeo, el parámetro *lpLoad* apunta a una estructura [**OVLY de carga de \_ \_ \_ parms MCI**](mci-ovly-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d7654-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7654-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7654-129">Requirements</span></span>



| <span data-ttu-id="d7654-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7654-130">Requirement</span></span> | <span data-ttu-id="d7654-131">Value</span><span class="sxs-lookup"><span data-stu-id="d7654-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7654-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7654-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7654-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7654-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7654-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7654-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7654-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7654-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7654-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7654-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7654-137"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7654-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7654-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7654-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7654-139">MCI</span><span class="sxs-lookup"><span data-stu-id="d7654-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d7654-140">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d7654-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

