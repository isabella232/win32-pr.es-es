---
description: Contiene un puntero al Administrador de dispositivos de DXGI para el escritor del receptor.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: MF_SINK_WRITER_D3D_MANAGER atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716951"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="c1c5e-103">\_Atributo de \_ Administrador de D3D del escritor de receptor MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="c1c5e-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="c1c5e-104">Contiene un puntero al Administrador de dispositivos de DXGI para el [escritor del receptor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="c1c5e-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="c1c5e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c1c5e-105">Data type</span></span>

<span data-ttu-id="c1c5e-106">**IMFDXGIDeviceManager \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="c1c5e-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c5e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1c5e-107">Remarks</span></span>

<span data-ttu-id="c1c5e-108">El valor de este atributo es un puntero a la interfaz [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="c1c5e-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="c1c5e-109">Use este atributo para proporcionar un dispositivo Direct3D para cualquier codificador de vídeo o receptor de medios cargados por el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="c1c5e-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="c1c5e-110">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="c1c5e-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="c1c5e-111">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="c1c5e-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="c1c5e-112">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="c1c5e-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="c1c5e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1c5e-113">Requirements</span></span>



| <span data-ttu-id="c1c5e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1c5e-114">Requirement</span></span> | <span data-ttu-id="c1c5e-115">Value</span><span class="sxs-lookup"><span data-stu-id="c1c5e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c5e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1c5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c5e-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c1c5e-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c1c5e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1c5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c5e-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c1c5e-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c1c5e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1c5e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c5e-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c5e-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c5e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1c5e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c5e-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1c5e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1c5e-124">Escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="c1c5e-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




