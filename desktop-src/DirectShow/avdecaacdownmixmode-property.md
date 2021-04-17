---
description: Especifica si un descodificador AAC usa ecuaciones downmix de estéreo estándar MPEG-2/MPEG-4, o usa un downmix no estándar.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propiedad AVDecAACDownmixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686382"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="749db-103">Propiedad AVDecAACDownmixMode</span><span class="sxs-lookup"><span data-stu-id="749db-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="749db-104">Especifica si un descodificador AAC usa ecuaciones downmix de estéreo estándar MPEG-2/MPEG-4, o usa un downmix no estándar.</span><span class="sxs-lookup"><span data-stu-id="749db-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="749db-105">Un ejemplo de downmix no estándar es el que se define en el documento ARIB STD-B21, versión 4,4.</span><span class="sxs-lookup"><span data-stu-id="749db-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="749db-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="749db-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="749db-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="749db-107">Data type</span></span>

<span data-ttu-id="749db-108">**UINT32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="749db-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="749db-109">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="749db-109">Property GUID</span></span>

<span data-ttu-id="749db-110">**CODECAPI \_ AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="749db-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="749db-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="749db-111">Property value</span></span>

<span data-ttu-id="749db-112">El valor de esta propiedad es un miembro de la enumeración [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="749db-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="749db-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="749db-113">Requirements</span></span>



| <span data-ttu-id="749db-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="749db-114">Requirement</span></span> | <span data-ttu-id="749db-115">Value</span><span class="sxs-lookup"><span data-stu-id="749db-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="749db-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="749db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="749db-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="749db-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="749db-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="749db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="749db-119">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="749db-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="749db-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="749db-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="749db-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="749db-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="749db-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="749db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749db-123">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="749db-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="749db-124">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="749db-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

