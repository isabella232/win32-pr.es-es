---
title: Comando MCI_CAPTURE (mmsystem. h)
description: El \_ comando MCI Capture captura el contenido del búfer de fotogramas y lo almacena en un archivo especificado. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- Comando de MCI_CAPTURE de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996703"
---
# <a name="mci_capture-command"></a><span data-ttu-id="02a39-105">\_Comando MCI Capture</span><span class="sxs-lookup"><span data-stu-id="02a39-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="02a39-106">El \_ comando MCI Capture captura el contenido del búfer de fotogramas y lo almacena en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="02a39-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="02a39-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="02a39-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="02a39-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="02a39-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="02a39-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02a39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02a39-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="02a39-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="02a39-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="02a39-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="02a39-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="02a39-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="02a39-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="02a39-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="02a39-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="02a39-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="02a39-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span><span class="sxs-lookup"><span data-stu-id="02a39-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="02a39-116">Puntero a una estructura de [**\_ \_ \_ parms de captura DGV de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="02a39-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02a39-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02a39-117">Return Value</span></span>

<span data-ttu-id="02a39-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="02a39-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a39-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02a39-119">Remarks</span></span>

<span data-ttu-id="02a39-120">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="02a39-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="02a39-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_ \_ captura de DGV MCI \_ como</span><span class="sxs-lookup"><span data-stu-id="02a39-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="02a39-122">El miembro **lpstrFileName** de la estructura identificada por *lpCapture* contiene una dirección de un búfer que especifica la ruta de acceso y el nombre de archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="02a39-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="02a39-123">(Esta marca es obligatoria).</span><span class="sxs-lookup"><span data-stu-id="02a39-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="02a39-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_ \_ captura de DGV \_ de MCI en</span><span class="sxs-lookup"><span data-stu-id="02a39-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="02a39-125">El miembro **RC** de la estructura identificada por *lpCapture* contiene un rectángulo válido.</span><span class="sxs-lookup"><span data-stu-id="02a39-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="02a39-126">El rectángulo especifica la región rectangular dentro del búfer de fotogramas que se recorta y se guarda en el disco.</span><span class="sxs-lookup"><span data-stu-id="02a39-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="02a39-127">Si se omite, el valor predeterminado de la región recortado es el rectángulo especificado o predeterminado en un comando anterior de [MCI \_ Put](mci-put.md) que especifica el área de origen para esta instancia del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02a39-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02a39-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02a39-128">Requirements</span></span>



| <span data-ttu-id="02a39-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a39-129">Requirement</span></span> | <span data-ttu-id="02a39-130">Value</span><span class="sxs-lookup"><span data-stu-id="02a39-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a39-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02a39-131">Minimum supported client</span></span><br/> | <span data-ttu-id="02a39-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="02a39-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="02a39-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02a39-133">Minimum supported server</span></span><br/> | <span data-ttu-id="02a39-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02a39-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02a39-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02a39-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="02a39-136"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02a39-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a39-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a39-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a39-138">MCI</span><span class="sxs-lookup"><span data-stu-id="02a39-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="02a39-139">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="02a39-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

