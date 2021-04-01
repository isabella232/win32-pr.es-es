---
description: Especifica si la aplicación requiere compatibilidad con Microsoft Direct3D en el lector de origen o el escritor de receptores.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279045"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="d6209-103">MF \_ ReadWrite \_ ( \_ atributo opcional)</span><span class="sxs-lookup"><span data-stu-id="d6209-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="d6209-104">Especifica si la aplicación requiere compatibilidad con Microsoft Direct3D en el [lector de origen](source-reader.md) o el escritor de [receptores](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="d6209-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="d6209-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d6209-105">Data type</span></span>

<span data-ttu-id="d6209-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d6209-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6209-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6209-107">Remarks</span></span>

<span data-ttu-id="d6209-108">Este atributo solo se aplica si la aplicación habilita la compatibilidad con Direct3D mediante el atributo de administrador de D3D del [ \_ lector de código fuente MF \_ \_ \_ ](mf-source-reader-d3d-manager.md) o el atributo de [ \_ \_ \_ \_ Administrador de recepción de receptor MF](mf-sink-writer-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="d6209-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="d6209-109">Si la aplicación habilita la compatibilidad con Direct3D, el lector de origen y el escritor del receptor intentarán asignar las superficies de Direct3D para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="d6209-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="d6209-110">Si se produce un error en esta y el \_ \_ atributo opcional MF ReadWrite D3D \_ es **true**, el sistema de escritura de origen/receptor de lectura revertirá a la asignación de superficies de vídeo en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="d6209-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="d6209-111">De lo contrario, si no se pueden asignar superficies de Direct3D y MF \_ ReadWrite \_ \_ opcional es **false**, se produce un error durante el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="d6209-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="d6209-112">Si la aplicación no habilita la compatibilidad con Direct3D, el sistema de escritura del receptor o el lector de origen usa la memoria del sistema y omite el valor de MF \_ ReadWrite ( \_ opcional) \_ .</span><span class="sxs-lookup"><span data-stu-id="d6209-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="d6209-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d6209-113">This attribute is optional.</span></span> <span data-ttu-id="d6209-114">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d6209-114">The default value is **FALSE**.</span></span> <span data-ttu-id="d6209-115">Establezca el atributo al crear el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="d6209-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6209-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6209-116">Requirements</span></span>



| <span data-ttu-id="d6209-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6209-117">Requirement</span></span> | <span data-ttu-id="d6209-118">Value</span><span class="sxs-lookup"><span data-stu-id="d6209-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6209-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6209-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6209-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6209-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6209-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6209-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6209-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6209-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6209-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6209-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6209-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6209-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6209-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6209-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6209-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6209-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6209-127">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="d6209-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6209-128">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="d6209-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




