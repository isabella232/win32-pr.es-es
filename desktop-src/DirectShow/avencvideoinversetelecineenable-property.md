---
description: Especifica si el codificador realiza telecine inversa.
ms.assetid: 3467b0c8-c27d-448a-8cbf-971307e4c408
title: Propiedad AVEncVideoInverseTelecineEnable (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31eac80651eb80d933c4f40ef22303c4858783d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152494"
---
# <a name="avencvideoinversetelecineenable-property"></a><span data-ttu-id="7ad88-103">Propiedad AVEncVideoInverseTelecineEnable</span><span class="sxs-lookup"><span data-stu-id="7ad88-103">AVEncVideoInverseTelecineEnable property</span></span>

<span data-ttu-id="7ad88-104">Especifica si el codificador realiza telecine inversa.</span><span class="sxs-lookup"><span data-stu-id="7ad88-104">Specifies whether the encoder performs inverse telecine.</span></span>

<span data-ttu-id="7ad88-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7ad88-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ad88-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7ad88-106">Data type</span></span>

<span data-ttu-id="7ad88-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="7ad88-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7ad88-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="7ad88-108">Property GUID</span></span>

<span data-ttu-id="7ad88-109">**CODECAPI \_ AVEncVideoInverseTelecineEnable**</span><span class="sxs-lookup"><span data-stu-id="7ad88-109">**CODECAPI\_AVEncVideoInverseTelecineEnable**</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad88-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ad88-110">Remarks</span></span>

<span data-ttu-id="7ad88-111">Si el valor es **Variant \_ true**, el codificador realiza telecine inversa.</span><span class="sxs-lookup"><span data-stu-id="7ad88-111">If the value is **VARIANT\_TRUE**, the encoder performs inverse telecine.</span></span> <span data-ttu-id="7ad88-112">Si no se requiere telecine inversa, establezca esta propiedad en **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="7ad88-112">If inverse telecine is not required, set this property to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="7ad88-113">Para realizar telecine inversa fuera del codificador, establezca esta propiedad en **Variant \_ false** y establezca la propiedad [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) en eAVEncVideoOutputScan \_ SameAsInput.</span><span class="sxs-lookup"><span data-stu-id="7ad88-113">To perform inverse telecine outside of the encoder, set this property to **VARIANT\_FALSE** and set the [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md) property to eAVEncVideoOutputScan\_SameAsInput.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad88-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ad88-114">Requirements</span></span>



| <span data-ttu-id="7ad88-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ad88-115">Requirement</span></span> | <span data-ttu-id="7ad88-116">Value</span><span class="sxs-lookup"><span data-stu-id="7ad88-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad88-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ad88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad88-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="7ad88-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7ad88-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ad88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad88-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="7ad88-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7ad88-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ad88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ad88-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad88-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad88-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ad88-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad88-124">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="7ad88-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7ad88-125">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7ad88-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




