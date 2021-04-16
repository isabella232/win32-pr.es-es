---
description: Detiene el paso de codificación actual o consulta si la fase de codificación actual es la última.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propiedad AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495640"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="e17ef-103">Propiedad AVEncCommonPassEnd</span><span class="sxs-lookup"><span data-stu-id="e17ef-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="e17ef-104">Detiene el paso de codificación actual o consulta si la fase de codificación actual es la última.</span><span class="sxs-lookup"><span data-stu-id="e17ef-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="e17ef-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e17ef-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e17ef-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e17ef-106">Data type</span></span>

<span data-ttu-id="e17ef-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="e17ef-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e17ef-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="e17ef-108">Property GUID</span></span>

<span data-ttu-id="e17ef-109">**CODECAPI \_ AVEncCommonPassEnd**</span><span class="sxs-lookup"><span data-stu-id="e17ef-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="e17ef-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e17ef-110">Remarks</span></span>

<span data-ttu-id="e17ef-111">Al establecer esta propiedad en **Variant \_ true** , finaliza la fase de codificación actual.</span><span class="sxs-lookup"><span data-stu-id="e17ef-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="e17ef-112">Al establecer esta propiedad en **Variant \_ false** se termina la codificación Multipass.</span><span class="sxs-lookup"><span data-stu-id="e17ef-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="e17ef-113">Al leer esta propiedad, se consulta si la fase de codificación actual es la última.</span><span class="sxs-lookup"><span data-stu-id="e17ef-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="e17ef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e17ef-114">Requirements</span></span>



| <span data-ttu-id="e17ef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e17ef-115">Requirement</span></span> | <span data-ttu-id="e17ef-116">Value</span><span class="sxs-lookup"><span data-stu-id="e17ef-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e17ef-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e17ef-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="e17ef-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e17ef-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e17ef-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="e17ef-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e17ef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e17ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e17ef-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e17ef-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e17ef-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e17ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17ef-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="e17ef-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e17ef-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e17ef-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




