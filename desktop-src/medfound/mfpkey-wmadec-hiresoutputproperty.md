---
description: Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Propiedad MFPKEY_WMADEC_HIRESOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706131"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="c3ede-103">\_ \_ Propiedad HIRESOUTPUT de MFPKEY WMADEC</span><span class="sxs-lookup"><span data-stu-id="c3ede-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="c3ede-104">Especifica si el descodificador de audio debe proporcionar una salida de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="c3ede-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c3ede-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c3ede-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c3ede-106">g \_ wszWMACHiResOutput</span><span class="sxs-lookup"><span data-stu-id="c3ede-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="c3ede-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c3ede-107">Data Type</span></span>

<span data-ttu-id="c3ede-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c3ede-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="c3ede-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c3ede-109">Default Value</span></span>

<span data-ttu-id="c3ede-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="c3ede-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ede-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3ede-111">Remarks</span></span>

<span data-ttu-id="c3ede-112">Establezca esta propiedad en VARIANT \_ true para descodificar el contenido de audio multicanal o de 24 bits, o audio con una velocidad de muestra superior a 48.000 Hz.</span><span class="sxs-lookup"><span data-stu-id="c3ede-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="c3ede-113">Si el contenido se codifica en alta resolución, pero esta propiedad es \_ la variante falsa, se aplican los comportamientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3ede-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="c3ede-114">La salida de DMO se limitará a un estéreo de 16 bits 48-KHz.</span><span class="sxs-lookup"><span data-stu-id="c3ede-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="c3ede-115">La MFT enumerará los modos de salida que están limitados a 16 bits y no implican cambios en el número de canales o la frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="c3ede-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="c3ede-116">Las propiedades de audio de alta resolución se pasan en una estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , no en [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3ede-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="c3ede-117">La salida de alta resolución solo está disponible si el descodificador se ejecuta en Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="c3ede-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="c3ede-118">Puede establecer esta propiedad independientemente del sistema operativo en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3ede-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="c3ede-119">En las versiones de Windows anteriores a Windows XP, el descodificador omitirá esta configuración y entregará la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="c3ede-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="c3ede-120">Muchos jugadores (incluidos Windows Media Player series 9 y versiones posteriores) establecen este valor para todo el contenido.</span><span class="sxs-lookup"><span data-stu-id="c3ede-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ede-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ede-121">Requirements</span></span>



| <span data-ttu-id="c3ede-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ede-122">Requirement</span></span> | <span data-ttu-id="c3ede-123">Value</span><span class="sxs-lookup"><span data-stu-id="c3ede-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ede-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3ede-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ede-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c3ede-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c3ede-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3ede-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ede-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3ede-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c3ede-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3ede-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3ede-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ede-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ede-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3ede-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ede-131">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3ede-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
