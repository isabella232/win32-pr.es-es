---
description: Deshabilita el uso de complementos de cámara posteriores al procesamiento por el lector de origen.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278922"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="15e11-103">\_Lector de código fuente MF \_ \_ deshabilitar \_ complemento de cámara ( \_ atributo)</span><span class="sxs-lookup"><span data-stu-id="15e11-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="15e11-104">Deshabilita el uso de complementos de cámara posteriores al procesamiento por el [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="15e11-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="15e11-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="15e11-105">Data type</span></span>

<span data-ttu-id="15e11-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="15e11-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="15e11-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15e11-107">Remarks</span></span>

<span data-ttu-id="15e11-108">Este atributo se aplica cuando el lector de origen se usa con un origen de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="15e11-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="15e11-109">Si este atributo es **true**, impide que el lector de código fuente cargue los complementos posteriores al procesamiento que pueda proporcionar la cámara.</span><span class="sxs-lookup"><span data-stu-id="15e11-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="15e11-110">De lo contrario, de forma predeterminada, el lector de código fuente los cargará.</span><span class="sxs-lookup"><span data-stu-id="15e11-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="15e11-111">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="15e11-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="15e11-112">Establezca el atributo al crear el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="15e11-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e11-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15e11-113">Requirements</span></span>



| <span data-ttu-id="15e11-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15e11-114">Requirement</span></span> | <span data-ttu-id="15e11-115">Value</span><span class="sxs-lookup"><span data-stu-id="15e11-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e11-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15e11-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15e11-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="15e11-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="15e11-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15e11-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15e11-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="15e11-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="15e11-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15e11-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e11-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e11-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e11-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="15e11-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e11-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15e11-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15e11-124">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="15e11-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




