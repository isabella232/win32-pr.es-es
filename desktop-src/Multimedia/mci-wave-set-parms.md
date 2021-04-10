---
title: MCI_WAVE_SET_PARMS estructura (Mciapi. h)
description: La \_ estructura parms de MCI Wave \_ set \_ contiene información para el \_ comando MCI set para dispositivos de audio de forma de onda.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Estructura de MCI_WAVE_SET_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905571"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="8479c-104">\_Estructura parms de MCI Wave \_ set \_</span><span class="sxs-lookup"><span data-stu-id="8479c-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="8479c-105">La estructura **parms de MCI \_ Wave \_ set \_** contiene información para el comando [**MCI \_ set**](mci-set.md) para dispositivos de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="8479c-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8479c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8479c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="8479c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8479c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8479c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8479c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8479c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="8479c-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-111">Formato de hora del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8479c-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="8479c-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-113">Número de canal para la salida de audio.</span><span class="sxs-lookup"><span data-stu-id="8479c-113">Channel number for audio output.</span></span> <span data-ttu-id="8479c-114">Se usa normalmente al activar o desactivar un canal.</span><span class="sxs-lookup"><span data-stu-id="8479c-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-115">**wInput**</span><span class="sxs-lookup"><span data-stu-id="8479c-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-116">Canal de entrada de audio.</span><span class="sxs-lookup"><span data-stu-id="8479c-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-117">**wOutput**</span><span class="sxs-lookup"><span data-stu-id="8479c-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-118">Dispositivo de salida que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="8479c-118">Output device to use.</span></span> <span data-ttu-id="8479c-119">Por ejemplo, este valor podría ser 2 Si un sistema tuviera dos tarjetas de sonido instaladas.</span><span class="sxs-lookup"><span data-stu-id="8479c-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-120">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="8479c-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-121">Formato de los datos de audio de forma de onda, como PCM con formato de onda \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8479c-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="8479c-122">Los valores posibles se definen en Mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="8479c-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="8479c-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8479c-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-125">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="8479c-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-126">Mono (1) o estéreo (2).</span><span class="sxs-lookup"><span data-stu-id="8479c-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="8479c-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="8479c-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8479c-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-129">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="8479c-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-130">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="8479c-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-131">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="8479c-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-132">Velocidad de muestra en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="8479c-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-133">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="8479c-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-134">Alineación de bloque de los datos.</span><span class="sxs-lookup"><span data-stu-id="8479c-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="8479c-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-136">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8479c-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-137">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="8479c-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-138">Bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="8479c-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="8479c-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="8479c-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="8479c-140">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8479c-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8479c-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8479c-141">Remarks</span></span>

<span data-ttu-id="8479c-142">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="8479c-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8479c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8479c-143">Requirements</span></span>



| <span data-ttu-id="8479c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8479c-144">Requirement</span></span> | <span data-ttu-id="8479c-145">Value</span><span class="sxs-lookup"><span data-stu-id="8479c-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8479c-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8479c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8479c-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8479c-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8479c-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8479c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8479c-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8479c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8479c-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8479c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8479c-151"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8479c-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8479c-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="8479c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8479c-153">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8479c-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8479c-154">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="8479c-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8479c-155">**MCI \_ set**</span><span class="sxs-lookup"><span data-stu-id="8479c-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="8479c-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8479c-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

