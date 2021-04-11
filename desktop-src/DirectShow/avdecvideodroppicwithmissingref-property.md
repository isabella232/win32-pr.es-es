---
description: Especifica si el descodificador quita las tramas dentro de las que faltan fotogramas de referencia.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propiedad AVDecVideoDropPicWithMissingRef (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274690"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="db475-103">Propiedad AVDecVideoDropPicWithMissingRef</span><span class="sxs-lookup"><span data-stu-id="db475-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="db475-104">Especifica si el descodificador quita las tramas dentro de las que faltan fotogramas de referencia.</span><span class="sxs-lookup"><span data-stu-id="db475-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="db475-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="db475-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="db475-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="db475-106">Data type</span></span>

<span data-ttu-id="db475-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="db475-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="db475-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="db475-108">Property GUID</span></span>

<span data-ttu-id="db475-109">**CODECAPI \_ AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="db475-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="db475-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db475-110">Remarks</span></span>

<span data-ttu-id="db475-111">Si el fragmentada está dañado, es posible que falten fotogramas de referencia en un fotograma.</span><span class="sxs-lookup"><span data-stu-id="db475-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="db475-112">Si el valor de esta propiedad es **Variant \_ true**, el descodificador quita el marco.</span><span class="sxs-lookup"><span data-stu-id="db475-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="db475-113">Si el valor es **Variant \_ false**, el descodificador intenta descodificar el fotograma, utilizando uno o más fotogramas cercanos como fotogramas de referencia.</span><span class="sxs-lookup"><span data-stu-id="db475-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="db475-114">El marco descodificado resultante tendrá artefactos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="db475-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="db475-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db475-115">Requirements</span></span>



| <span data-ttu-id="db475-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db475-116">Requirement</span></span> | <span data-ttu-id="db475-117">Value</span><span class="sxs-lookup"><span data-stu-id="db475-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db475-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db475-118">Minimum supported client</span></span><br/> | <span data-ttu-id="db475-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="db475-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="db475-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db475-120">Minimum supported server</span></span><br/> | <span data-ttu-id="db475-121">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="db475-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="db475-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db475-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="db475-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db475-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db475-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="db475-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db475-125">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="db475-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="db475-126">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="db475-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




