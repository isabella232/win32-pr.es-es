---
description: Especifica el número máximo de ejemplos de salida que una transformación de Microsoft Media Foundation (MFT) tendrá pendiente en la canalización en cualquier momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275690"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="1497c-103">\_Atributo de \_ \_ \_ recuento de ejemplo de salida mínima de SA de MF \_</span><span class="sxs-lookup"><span data-stu-id="1497c-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="1497c-104">Especifica el número máximo de ejemplos de salida que una transformación de Microsoft Media Foundation (MFT) tendrá pendiente en la canalización en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="1497c-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="1497c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1497c-105">Data type</span></span>

<span data-ttu-id="1497c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1497c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1497c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1497c-107">Remarks</span></span>

<span data-ttu-id="1497c-108">Este atributo solo se aplica a MFTs que usan un búfer circular para asignar sus propios ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="1497c-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="1497c-109">Otros MFTs omiten este atributo.</span><span class="sxs-lookup"><span data-stu-id="1497c-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="1497c-110">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="1497c-110">To set this attribute:</span></span>

1.  <span data-ttu-id="1497c-111">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1497c-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="1497c-112">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.</span><span class="sxs-lookup"><span data-stu-id="1497c-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="1497c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1497c-113">Requirements</span></span>



| <span data-ttu-id="1497c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1497c-114">Requirement</span></span> | <span data-ttu-id="1497c-115">Value</span><span class="sxs-lookup"><span data-stu-id="1497c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1497c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1497c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1497c-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1497c-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1497c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1497c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1497c-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1497c-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1497c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1497c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1497c-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="1497c-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1497c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1497c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1497c-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1497c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1497c-124">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="1497c-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




