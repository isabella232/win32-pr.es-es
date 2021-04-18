---
description: Establece el número máximo de iteraciones de búsqueda que usará el origen de medios ASF cuando realice búsquedas iterativas.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: Propiedad MFPKEY_ASFMediaSource_IterativeSeek_Max_Count (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697970"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="1e61c-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_ propiedad Count Max</span><span class="sxs-lookup"><span data-stu-id="1e61c-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="1e61c-104">Establece el número máximo de iteraciones de búsqueda que usará el origen de medios ASF cuando realice búsquedas iterativas.</span><span class="sxs-lookup"><span data-stu-id="1e61c-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="1e61c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1e61c-105">Data type</span></span>

<span data-ttu-id="1e61c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1e61c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1e61c-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1e61c-107">PROPVARIANT member</span></span>

<span data-ttu-id="1e61c-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="1e61c-108">**ULONG**</span></span>

<span data-ttu-id="1e61c-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1e61c-109">VT\_UI4</span></span>

<span data-ttu-id="1e61c-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="1e61c-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1e61c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e61c-111">Remarks</span></span>

<span data-ttu-id="1e61c-112">Utilice esta propiedad para configurar el origen de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="1e61c-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="1e61c-113">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="1e61c-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="1e61c-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1e61c-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1e61c-115">Esta propiedad solo se aplica cuando está habilitada la búsqueda iterativa.</span><span class="sxs-lookup"><span data-stu-id="1e61c-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="1e61c-116">Para obtener más información, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="1e61c-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="1e61c-117">El intervalo válido de esta propiedad es \[ 1-10 \] , ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="1e61c-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="1e61c-118">Con un número mayor, la búsqueda iterativa tiende a ser más precisa, pero tarda más tiempo.</span><span class="sxs-lookup"><span data-stu-id="1e61c-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="1e61c-119">El valor predeterminado es 5.</span><span class="sxs-lookup"><span data-stu-id="1e61c-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e61c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e61c-120">Requirements</span></span>



| <span data-ttu-id="1e61c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e61c-121">Requirement</span></span> | <span data-ttu-id="1e61c-122">Value</span><span class="sxs-lookup"><span data-stu-id="1e61c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e61c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e61c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e61c-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="1e61c-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1e61c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e61c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e61c-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="1e61c-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1e61c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e61c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e61c-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e61c-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e61c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e61c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e61c-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e61c-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




