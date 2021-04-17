---
description: Valor que indica el tipo de sensor proporcionado por un origen de fotogramas, como color, infrarrojos o Depth.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659846"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="a567c-103">MF \_ MT \_ FRAMESOURCE \_ Types (atributo)</span><span class="sxs-lookup"><span data-stu-id="a567c-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="a567c-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a567c-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a567c-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a567c-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a567c-106">Valor que indica el tipo de sensor proporcionado por un origen de fotogramas, como color, infrarrojos o Depth.</span><span class="sxs-lookup"><span data-stu-id="a567c-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="a567c-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a567c-107">Data type</span></span>

<span data-ttu-id="a567c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a567c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a567c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a567c-109">Remarks</span></span>

<span data-ttu-id="a567c-110">Este valor debe ser un miembro de la enumeración [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a567c-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="a567c-111">Por compatibilidad con versiones anteriores, cuando este atributo no está definido en un tipo de medio, se supone que es **\_ MFFrameSourceTyes:: color**.</span><span class="sxs-lookup"><span data-stu-id="a567c-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a567c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a567c-112">Requirements</span></span>



| <span data-ttu-id="a567c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a567c-113">Requirement</span></span> | <span data-ttu-id="a567c-114">Value</span><span class="sxs-lookup"><span data-stu-id="a567c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a567c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a567c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a567c-116">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="a567c-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a567c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a567c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a567c-118">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="a567c-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a567c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a567c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a567c-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a567c-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
