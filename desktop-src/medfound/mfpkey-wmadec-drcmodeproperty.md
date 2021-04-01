---
description: Especifica el modo de control de intervalo dinámico que usará el descodificador de audio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Propiedad MFPKEY_WMADEC_DRCMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275851"
---
# <a name="mfpkey_wmadec_drcmode-property"></a><span data-ttu-id="18e9a-103">\_ \_ Propiedad DRCMODE de MFPKEY WMADEC</span><span class="sxs-lookup"><span data-stu-id="18e9a-103">MFPKEY\_WMADEC\_DRCMODE Property</span></span>

<span data-ttu-id="18e9a-104">Especifica el modo de control de intervalo dinámico que usará el descodificador de audio.</span><span class="sxs-lookup"><span data-stu-id="18e9a-104">Specifies the dynamic range control mode that the audio decoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="18e9a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="18e9a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="18e9a-106">g \_ wszWMACDRCSetting</span><span class="sxs-lookup"><span data-stu-id="18e9a-106">g\_wszWMACDRCSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="18e9a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="18e9a-107">Data Type</span></span>

<span data-ttu-id="18e9a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="18e9a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="18e9a-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="18e9a-109">Default Value</span></span>

<span data-ttu-id="18e9a-110">0</span><span class="sxs-lookup"><span data-stu-id="18e9a-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="18e9a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18e9a-111">Remarks</span></span>

<span data-ttu-id="18e9a-112">Este valor entero va de 0 a 2.</span><span class="sxs-lookup"><span data-stu-id="18e9a-112">This integer value ranges from 0 to 2.</span></span> <span data-ttu-id="18e9a-113">Cuanto mayor sea el valor, menor será el intervalo dinámico de la salida de audio sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="18e9a-113">The greater the value, the smaller the dynamic range of the uncompressed audio output.</span></span> <span data-ttu-id="18e9a-114">Un valor de 0 indica que el códec no realiza ningún control de intervalo dinámico, es decir, el códec no modificará el intervalo dinámico inherente del contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="18e9a-114">A value of 0 signals the codec to perform no dynamic range control, that is, the codec will not alter the inherent dynamic range of the encoded content.</span></span>

<span data-ttu-id="18e9a-115">Si este valor se establece en 1 o 2, el códec usará las siguientes propiedades para determinar el control de intervalo dinámico necesario:</span><span class="sxs-lookup"><span data-stu-id="18e9a-115">If this value is set to 1 or 2, the codec will use the following properties to determine the needed dynamic range control:</span></span>

-   [<span data-ttu-id="18e9a-116">MFPKEY \_ WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="18e9a-116">MFPKEY\_WMADRC\_AVGREF</span></span>](mfpkey-wmadrc-avgrefproperty.md)
-   [<span data-ttu-id="18e9a-117">MFPKEY \_ WMADRC \_ PEAKREF</span><span class="sxs-lookup"><span data-stu-id="18e9a-117">MFPKEY\_WMADRC\_PEAKREF</span></span>](mfpkey-wmadrc-peakrefproperty.md)
-   [<span data-ttu-id="18e9a-118">MFPKEY \_ WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="18e9a-118">MFPKEY\_WMADRC\_AVGTARGET</span></span>](mfpkey-wmadrc-avgtargetproperty.md)
-   [<span data-ttu-id="18e9a-119">MFPKEY \_ WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="18e9a-119">MFPKEY\_WMADRC\_PEAKTARGET</span></span>](mfpkey-wmadrc-peaktargetproperty.md)

<span data-ttu-id="18e9a-120">Si no proporciona valores de destino, el códec proporcionará el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="18e9a-120">If you do not provide target values, the codec will provide its own.</span></span>

## <a name="requirements"></a><span data-ttu-id="18e9a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e9a-121">Requirements</span></span>



| <span data-ttu-id="18e9a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e9a-122">Requirement</span></span> | <span data-ttu-id="18e9a-123">Value</span><span class="sxs-lookup"><span data-stu-id="18e9a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18e9a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18e9a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18e9a-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="18e9a-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="18e9a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18e9a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18e9a-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="18e9a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18e9a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18e9a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="18e9a-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18e9a-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e9a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="18e9a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e9a-131">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18e9a-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




