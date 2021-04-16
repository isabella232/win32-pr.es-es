---
title: Estructura de _WAVEFORMATEX
description: La estructura \_WAVEFORMATEX define el formato de datos de audio Waveform.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Estructura _WAVEFORMATEX Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699519"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="d6005-104">\_WAVEFORMATEX (estructura)</span><span class="sxs-lookup"><span data-stu-id="d6005-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="d6005-105">La estructura **\_ WAVEFORMATEX** define el formato de los datos de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="d6005-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6005-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6005-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="d6005-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6005-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d6005-108">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="d6005-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-109">Debe establecerse en un formato o en los formatos admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6005-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="d6005-110">Tenga en cuenta que en las versiones anteriores de Windows Media Administrador de dispositivos recomendamos usar \_ All Wave Format de WMDM \_ \_ para indicar la compatibilidad con todos los formatos.</span><span class="sxs-lookup"><span data-stu-id="d6005-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="d6005-111">Sin embargo, esto ya no se recomienda, ya que los distintos reproductores multimedia interpretarán esto de maneras diferentes y algunos dispositivos pueden reproducir realmente cualquier formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="d6005-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="d6005-112">Ahora se recomienda usar la enumeración de WMDM \_ \_ \_ valores válidos \_ de valores válidos \_ cualquier valor de la enumeración del formulario de enumeración de [**WMDM \_ propiedades de \_ \_ \_ valores \_ válidos**](wmdm-enum-prop-valid-values-form.md) , o bien especificar mejor un intervalo de formatos con la estructura de intervalo de valores de prop de [**WMDM \_ \_ \_**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="d6005-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6005-113">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="d6005-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-114">Número de canales en los datos de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="d6005-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="d6005-115">Los datos monoaural usan un canal y los datos estéreo usan dos canales.</span><span class="sxs-lookup"><span data-stu-id="d6005-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="d6005-116">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="d6005-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-117">Frecuencia de muestreo, en muestras por segundo (hercios), en la que se debe reproducir o grabar cada canal.</span><span class="sxs-lookup"><span data-stu-id="d6005-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="d6005-118">Los valores comunes para **nSamplesPerSec** son 8,0 kilohercios (kHz), 11,025 khz, 22,05 khz y 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="d6005-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="d6005-119">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="d6005-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-120">Velocidad de transferencia de datos media requerida para la etiqueta de formato, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="d6005-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="d6005-121">El software de reproducción y grabación puede calcular los tamaños de búfer mediante el miembro **nAvgBytesPerSec** .</span><span class="sxs-lookup"><span data-stu-id="d6005-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="d6005-122">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="d6005-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-123">Alineación de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d6005-123">Block alignment, in bytes.</span></span> <span data-ttu-id="d6005-124">La alineación de bloque es la unidad atómica mínima de datos para el tipo de formato **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="d6005-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="d6005-125">El software de reproducción y grabación debe procesar un múltiplo de **nBlockAlign** bytes de datos a la vez.</span><span class="sxs-lookup"><span data-stu-id="d6005-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="d6005-126">Los datos escritos y leídos de un dispositivo siempre deben empezar al principio de un bloque.</span><span class="sxs-lookup"><span data-stu-id="d6005-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="d6005-127">Por ejemplo, no es posible empezar a reproducir correctamente los datos PCM en medio de un ejemplo (es decir, en un límite que no está alineado con un bloque).</span><span class="sxs-lookup"><span data-stu-id="d6005-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="d6005-128">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="d6005-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-129">Bits por muestra para el tipo de formato **wFormatTag** .</span><span class="sxs-lookup"><span data-stu-id="d6005-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="d6005-130">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d6005-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d6005-131">Este miembro se omite.</span><span class="sxs-lookup"><span data-stu-id="d6005-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6005-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6005-132">Requirements</span></span>



| <span data-ttu-id="d6005-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6005-133">Requirement</span></span> | <span data-ttu-id="d6005-134">Value</span><span class="sxs-lookup"><span data-stu-id="d6005-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d6005-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6005-135">Header</span></span><br/> | <dl> <span data-ttu-id="d6005-136"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6005-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6005-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6005-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6005-138">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="d6005-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="d6005-139">**IMDSPStorage::CreateStorage**</span><span class="sxs-lookup"><span data-stu-id="d6005-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="d6005-140">**IMDSPStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="d6005-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="d6005-141">**IWMDMDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="d6005-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="d6005-142">**IWMDMOperation::GetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="d6005-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="d6005-143">**IWMDMOperation::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="d6005-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="d6005-144">**IWMDMStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="d6005-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="d6005-145">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="d6005-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





