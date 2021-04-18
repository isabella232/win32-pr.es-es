---
description: Indica que Moov se escribirá antes que el cuadro mdat en el archivo generado.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706431"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="fb165-103">MF \_ MPEG4SINK \_ MOOV \_ antes del \_ atributo MDAT</span><span class="sxs-lookup"><span data-stu-id="fb165-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="fb165-104">Indica que "Moov" se escribirá antes que el cuadro "mdat" en el archivo generado.</span><span class="sxs-lookup"><span data-stu-id="fb165-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="fb165-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fb165-105">Data type</span></span>

<span data-ttu-id="fb165-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fb165-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fb165-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb165-107">Remarks</span></span>

<span data-ttu-id="fb165-108">El comportamiento predeterminado del receptor de medios MPEG4 es escribir ' Moov ' después del cuadro ' mdat '.</span><span class="sxs-lookup"><span data-stu-id="fb165-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="fb165-109">La configuración de este atributo hace que el archivo generado escriba ' Moov ' delante del cuadro ' mdat '.</span><span class="sxs-lookup"><span data-stu-id="fb165-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="fb165-110">Para que el receptor MPEG4 use este atributo, la secuencia de bytes pasada no debe ser una búsqueda lenta o remota para.</span><span class="sxs-lookup"><span data-stu-id="fb165-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="fb165-111">Esta característica implica la copia de archivos/remuxing adicionales.</span><span class="sxs-lookup"><span data-stu-id="fb165-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb165-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb165-112">Requirements</span></span>



| <span data-ttu-id="fb165-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb165-113">Requirement</span></span> | <span data-ttu-id="fb165-114">Value</span><span class="sxs-lookup"><span data-stu-id="fb165-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb165-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb165-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fb165-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="fb165-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="fb165-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb165-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fb165-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="fb165-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fb165-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb165-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb165-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb165-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb165-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb165-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb165-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb165-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fb165-123">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="fb165-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




