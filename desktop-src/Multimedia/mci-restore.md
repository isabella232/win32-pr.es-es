---
title: Comando MCI_RESTORE (mmsystem. h)
description: El \_ comando MCI restore copia un mapa de bits de un archivo en el búfer de fotogramas. Los dispositivos de vídeo digital reconocen este comando. Este comando realiza la acción opuesta del comando MCI \_ Capture.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Comando de MCI_RESTORE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803259"
---
# <a name="mci_restore-command"></a><span data-ttu-id="2a07a-106">Comando de restauración de MCI \_</span><span class="sxs-lookup"><span data-stu-id="2a07a-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="2a07a-107">El \_ comando MCI restore copia un mapa de bits de un archivo en el búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2a07a-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="2a07a-108">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="2a07a-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="2a07a-109">Este comando realiza la acción opuesta del comando [MCI \_ Capture](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="2a07a-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="2a07a-110">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="2a07a-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="2a07a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a07a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a07a-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2a07a-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2a07a-113">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="2a07a-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2a07a-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2a07a-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2a07a-115">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="2a07a-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2a07a-116">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2a07a-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a07a-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span><span class="sxs-lookup"><span data-stu-id="2a07a-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="2a07a-118">Puntero a una estructura [**MCI \_ DGV \_ restore \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="2a07a-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a07a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a07a-119">Return Value</span></span>

<span data-ttu-id="2a07a-120">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2a07a-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a07a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a07a-121">Remarks</span></span>

<span data-ttu-id="2a07a-122">La implementación puede reconocer varios formatos de imagen, pero siempre se acepta un mapa de bits independiente del dispositivo (DIB) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2a07a-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="2a07a-123">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="2a07a-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="2a07a-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_ \_ restauración de DGV \_ de MCI desde</span><span class="sxs-lookup"><span data-stu-id="2a07a-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="2a07a-125">El miembro **lpstrFileName** de la estructura identificada por *lpRestore* contiene una dirección de un búfer que contiene el nombre de archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="2a07a-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="2a07a-126">El nombre de archivo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a07a-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="2a07a-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_ \_ restauración de MCI DGV \_ en</span><span class="sxs-lookup"><span data-stu-id="2a07a-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="2a07a-128">El miembro **RC** de la estructura identificada por *lpRestore* contiene un rectángulo válido.</span><span class="sxs-lookup"><span data-stu-id="2a07a-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="2a07a-129">El rectángulo especifica una región del búfer de fotogramas relativa a su origen.</span><span class="sxs-lookup"><span data-stu-id="2a07a-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="2a07a-130">El primer par de coordenadas especifica la esquina superior izquierda del rectángulo; el segundo par especifica el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="2a07a-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="2a07a-131">Si no se especifica esta marca, la imagen se copia en la esquina superior izquierda del búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2a07a-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a07a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a07a-132">Requirements</span></span>



| <span data-ttu-id="2a07a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a07a-133">Requirement</span></span> | <span data-ttu-id="2a07a-134">Value</span><span class="sxs-lookup"><span data-stu-id="2a07a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a07a-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a07a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2a07a-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2a07a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2a07a-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a07a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2a07a-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a07a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2a07a-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a07a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a07a-140"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a07a-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a07a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a07a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a07a-142">MCI</span><span class="sxs-lookup"><span data-stu-id="2a07a-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2a07a-143">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="2a07a-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

