---
description: Especifica el identificador de streaming de kernel (KS) de una secuencia en un dispositivo de captura de vídeo.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: MF_DEVICESTREAM_STREAM_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082351"
---
# <a name="mf_devicestream_stream_id-attribute"></a><span data-ttu-id="2bb62-103">\_Atributo de \_ \_ ID. de secuencia MF DEVICESTREAM</span><span class="sxs-lookup"><span data-stu-id="2bb62-103">MF\_DEVICESTREAM\_STREAM\_ID attribute</span></span>

<span data-ttu-id="2bb62-104">Especifica el identificador de streaming de kernel (KS) de una secuencia en un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2bb62-104">Specifies the kernel streaming (KS) identifier for a stream on a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bb62-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2bb62-105">Data type</span></span>

<span data-ttu-id="2bb62-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2bb62-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb62-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bb62-107">Remarks</span></span>

<span data-ttu-id="2bb62-108">Para obtener este atributo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2bb62-108">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="2bb62-109">Consulte el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="2bb62-109">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="2bb62-110">Llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2bb62-110">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="2bb62-111">Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="2bb62-111">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb62-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bb62-112">Requirements</span></span>



| <span data-ttu-id="2bb62-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bb62-113">Requirement</span></span> | <span data-ttu-id="2bb62-114">Value</span><span class="sxs-lookup"><span data-stu-id="2bb62-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb62-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb62-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb62-116">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bb62-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2bb62-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb62-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb62-118">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bb62-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2bb62-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bb62-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bb62-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bb62-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb62-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bb62-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb62-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bb62-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




