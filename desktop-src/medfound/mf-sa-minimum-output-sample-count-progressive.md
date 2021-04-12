---
description: Indica el número mínimo de muestras progresivas que la transformación de Microsoft Media Foundation (MFT) debe permitir que se pendientes en un momento dado.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277683"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="59477-103">Recuento de \_ \_ muestras de salida mínimas \_ de \_ \_ MF SA \_</span><span class="sxs-lookup"><span data-stu-id="59477-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="59477-104">Indica el número mínimo de muestras progresivas que la transformación de Microsoft Media Foundation (MFT) debe permitir que se pendientes en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="59477-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="59477-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="59477-105">Data type</span></span>

<span data-ttu-id="59477-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="59477-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="59477-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59477-107">Remarks</span></span>

<span data-ttu-id="59477-108">Este atributo solo se aplica a MFTs que usan un búfer circular para asignar sus propios ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="59477-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="59477-109">Otros MFTs omiten este atributo.</span><span class="sxs-lookup"><span data-stu-id="59477-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="59477-110">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="59477-110">To set this attribute:</span></span>

1.  <span data-ttu-id="59477-111">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="59477-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="59477-112">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.</span><span class="sxs-lookup"><span data-stu-id="59477-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="59477-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59477-113">Requirements</span></span>



| <span data-ttu-id="59477-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="59477-114">Requirement</span></span> | <span data-ttu-id="59477-115">Value</span><span class="sxs-lookup"><span data-stu-id="59477-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59477-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59477-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59477-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="59477-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="59477-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59477-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59477-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="59477-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="59477-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59477-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59477-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="59477-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59477-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="59477-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59477-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59477-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




