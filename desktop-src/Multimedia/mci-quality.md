---
title: Comando MCI_QUALITY (mmsystem. h)
description: El \_ comando MCI Quality define un nivel de calidad personalizado para la compresión de datos de audio, vídeo o imagen fija. Los dispositivos de vídeo digital reconocen este comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Comando de MCI_QUALITY de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421911"
---
# <a name="mci_quality-command"></a><span data-ttu-id="c8543-105">Comando de calidad de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c8543-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="c8543-106">El \_ comando MCI Quality define un nivel de calidad personalizado para la compresión de datos de audio, vídeo o imagen fija.</span><span class="sxs-lookup"><span data-stu-id="c8543-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="c8543-107">Los dispositivos de vídeo digital reconocen este comando.</span><span class="sxs-lookup"><span data-stu-id="c8543-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c8543-108">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8543-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="c8543-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8543-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8543-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c8543-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c8543-111">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="c8543-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c8543-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c8543-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c8543-113">\_Notificación de MCI, \_ espera de MCI o \_ prueba de MCI.</span><span class="sxs-lookup"><span data-stu-id="c8543-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c8543-114">Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c8543-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8543-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span><span class="sxs-lookup"><span data-stu-id="c8543-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="c8543-116">Puntero a una estructura de [**\_ \_ \_ parms de calidad DGV de MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="c8543-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8543-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8543-117">Return Value</span></span>

<span data-ttu-id="c8543-118">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c8543-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8543-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8543-119">Remarks</span></span>

<span data-ttu-id="c8543-120">El nombre definido para este nivel de calidad se puede usar al establecer el audio, el vídeo o la calidad continua con los comandos [MCI \_ SETAUDIO](mci-setaudio.md) y [MCI \_ SETVIDEO](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="c8543-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="c8543-121">Las siguientes marcas adicionales se aplican a los dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="c8543-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="c8543-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_alg calidad de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c8543-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="c8543-123">El miembro **lpstrAlgorithm** de la estructura identificada por *lpQuality* contiene una dirección de un búfer que contiene el nombre del algoritmo.</span><span class="sxs-lookup"><span data-stu-id="c8543-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="c8543-124">Este algoritmo debe ser compatible con el controlador de dispositivo y debe ser compatible con el descriptor de vídeo, de audio o de vídeo que se usa.</span><span class="sxs-lookup"><span data-stu-id="c8543-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="c8543-125">Si se omite esta marca, se utiliza el algoritmo actual.</span><span class="sxs-lookup"><span data-stu-id="c8543-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="c8543-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_cuadro de diálogo calidad de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c8543-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="c8543-127">El controlador de dispositivo debe mostrar un cuadro de diálogo para especificar el nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="c8543-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="c8543-128">El cuadro de diálogo tiene campos específicos del algoritmo utilizados internamente por el controlador de dispositivo para crear una estructura que describe un nivel de calidad específico.</span><span class="sxs-lookup"><span data-stu-id="c8543-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="c8543-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_controlador de calidad de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c8543-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="c8543-130">El miembro **dwHandle** de la estructura identificada por *lpQuality* contiene un identificador para una estructura.</span><span class="sxs-lookup"><span data-stu-id="c8543-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="c8543-131">La estructura contiene datos específicos del algoritmo que describen el nivel de calidad específico.</span><span class="sxs-lookup"><span data-stu-id="c8543-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="c8543-132">El formato de las estructuras para los algoritmos depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8543-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="c8543-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_elemento de calidad de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c8543-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="c8543-134">Una constante que indica el tipo de algoritmo se incluye en el miembro **dwItem** de la estructura identificada por *lpQuality*.</span><span class="sxs-lookup"><span data-stu-id="c8543-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="c8543-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_nombre de calidad de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c8543-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="c8543-136">El miembro **lpstrName** de la estructura identificada por *lpQuality* contiene una dirección de un búfer que contiene el descriptor de calidad.</span><span class="sxs-lookup"><span data-stu-id="c8543-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8543-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8543-137">Requirements</span></span>



| <span data-ttu-id="c8543-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8543-138">Requirement</span></span> | <span data-ttu-id="c8543-139">Value</span><span class="sxs-lookup"><span data-stu-id="c8543-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8543-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8543-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c8543-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8543-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8543-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8543-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c8543-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8543-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8543-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8543-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8543-145"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8543-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8543-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8543-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8543-147">MCI</span><span class="sxs-lookup"><span data-stu-id="c8543-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c8543-148">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c8543-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

