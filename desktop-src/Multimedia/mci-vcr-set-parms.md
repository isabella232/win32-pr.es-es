---
title: MCI_VCR_SET_PARMS estructura (VCR. h)
description: La estructura de parms de VCR de MCI \_ \_ \_ contiene parámetros para el \_ comando MCI set para los grabadores de casete de vídeo.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- Estructura de MCI_VCR_SET_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422553"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="eedc3-104">\_Estructura parms del vídeo de MCI \_ set \_</span><span class="sxs-lookup"><span data-stu-id="eedc3-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="eedc3-105">La estructura de **\_ \_ \_ parms de VCR de MCI** contiene parámetros para el comando [**MCI \_ set**](mci-set.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eedc3-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="eedc3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eedc3-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="eedc3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="eedc3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="eedc3-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="eedc3-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="eedc3-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="eedc3-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-111">Formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="eedc3-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="eedc3-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="eedc3-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-114">**dwTimeMode**</span><span class="sxs-lookup"><span data-stu-id="eedc3-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-115">Constante que especifica el origen de tiempo utilizado por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eedc3-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="eedc3-116">El origen de tiempo es un código de tiempo que se graba en una cinta de vídeo o los contadores del dispositivo que tienen en cuenta el movimiento de la cinta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eedc3-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-117">**dwRecordFormat**</span><span class="sxs-lookup"><span data-stu-id="eedc3-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-118">Velocidad de grabación.</span><span class="sxs-lookup"><span data-stu-id="eedc3-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-119">**dwCounterFormat**</span><span class="sxs-lookup"><span data-stu-id="eedc3-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-120">Formato de un nuevo valor de tiempo de contador.</span><span class="sxs-lookup"><span data-stu-id="eedc3-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-121">**dwIndex**</span><span class="sxs-lookup"><span data-stu-id="eedc3-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-122">Contenido de la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="eedc3-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-123">**dwTracking**</span><span class="sxs-lookup"><span data-stu-id="eedc3-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-124">Ajuste de velocidad usado cuando se realiza el seguimiento de la velocidad de reproducción de VCR.</span><span class="sxs-lookup"><span data-stu-id="eedc3-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-125">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="eedc3-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-126">Velocidad de reproducción utilizada por el dispositivo como un entero.</span><span class="sxs-lookup"><span data-stu-id="eedc3-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="eedc3-127">La velocidad de reproducción normal es 1000, la velocidad doble es 2000 y la velocidad media es 500.</span><span class="sxs-lookup"><span data-stu-id="eedc3-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-128">**dwLength**</span><span class="sxs-lookup"><span data-stu-id="eedc3-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-129">Longitud de la cinta de vídeo cuando el dispositivo no detecta la longitud.</span><span class="sxs-lookup"><span data-stu-id="eedc3-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-130">**dwCounter**</span><span class="sxs-lookup"><span data-stu-id="eedc3-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-131">Nuevo valor del contador.</span><span class="sxs-lookup"><span data-stu-id="eedc3-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-132">**dwClock**</span><span class="sxs-lookup"><span data-stu-id="eedc3-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-133">Nueva hora de reloj.</span><span class="sxs-lookup"><span data-stu-id="eedc3-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-134">**dwPauseTimeout**</span><span class="sxs-lookup"><span data-stu-id="eedc3-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-135">Nuevo valor de tiempo de espera para el comando pausar.</span><span class="sxs-lookup"><span data-stu-id="eedc3-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-136">**dwPrerollDuration**</span><span class="sxs-lookup"><span data-stu-id="eedc3-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-137">Duración de la cinta de vídeo necesaria para estabilizar la salida del VCR.</span><span class="sxs-lookup"><span data-stu-id="eedc3-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="eedc3-138">**dwPostrollDuration**</span><span class="sxs-lookup"><span data-stu-id="eedc3-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="eedc3-139">Longitud de la cinta de vídeo necesaria para frenar el transporte de VCR cuando se emite un comando [**MCI \_ Stop**](mci-stop.md) o [**MCI \_ PAUSE**](mci-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="eedc3-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eedc3-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eedc3-140">Remarks</span></span>

<span data-ttu-id="eedc3-141">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="eedc3-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="eedc3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eedc3-142">Requirements</span></span>



| <span data-ttu-id="eedc3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="eedc3-143">Requirement</span></span> | <span data-ttu-id="eedc3-144">Value</span><span class="sxs-lookup"><span data-stu-id="eedc3-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eedc3-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eedc3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="eedc3-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eedc3-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eedc3-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eedc3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="eedc3-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eedc3-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eedc3-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eedc3-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="eedc3-150"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="eedc3-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eedc3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="eedc3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eedc3-152">**MCI**</span><span class="sxs-lookup"><span data-stu-id="eedc3-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="eedc3-153">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="eedc3-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="eedc3-154">**pausa de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="eedc3-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="eedc3-155">**MCI \_ set**</span><span class="sxs-lookup"><span data-stu-id="eedc3-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="eedc3-156">**detención de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="eedc3-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="eedc3-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eedc3-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

