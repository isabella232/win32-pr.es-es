---
description: Especifica el nivel de volumen medio del contenido de audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Propiedad MFPKEY_WMADRC_AVGREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666781"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="62b71-103">\_ \_ Propiedad AVGREF de MFPKEY WMADRC</span><span class="sxs-lookup"><span data-stu-id="62b71-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="62b71-104">Especifica el nivel de volumen medio del contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="62b71-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="62b71-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="62b71-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="62b71-106">g \_ wszWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="62b71-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="62b71-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="62b71-107">Data Type</span></span>

<span data-ttu-id="62b71-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="62b71-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="62b71-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62b71-109">Remarks</span></span>

<span data-ttu-id="62b71-110">Puede obtener este valor desde el codificador una vez procesado el contenido.</span><span class="sxs-lookup"><span data-stu-id="62b71-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="62b71-111">Este valor también se puede establecer en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="62b71-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="62b71-112">Para obtener más información sobre el control de intervalo dinámico, vea el artículo Web [Windows Media Audio características de códecs profesionales](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="62b71-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="62b71-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62b71-113">Requirements</span></span>



| <span data-ttu-id="62b71-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62b71-114">Requirement</span></span> | <span data-ttu-id="62b71-115">Value</span><span class="sxs-lookup"><span data-stu-id="62b71-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62b71-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62b71-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62b71-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="62b71-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="62b71-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62b71-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62b71-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="62b71-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62b71-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62b71-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62b71-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62b71-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b71-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="62b71-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b71-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62b71-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
