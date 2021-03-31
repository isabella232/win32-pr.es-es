---
description: Especifica si el descodificador debe realizar Lt-Rt pliegue.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Propiedad MFPKEY_WMADEC_LTRTOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155388"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="95f9a-103">\_ \_ Propiedad LTRTOUTPUT de MFPKEY WMADEC</span><span class="sxs-lookup"><span data-stu-id="95f9a-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="95f9a-104">Especifica si el descodificador debe realizar Lt-Rt pliegue.</span><span class="sxs-lookup"><span data-stu-id="95f9a-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="95f9a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="95f9a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="95f9a-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="95f9a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="95f9a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="95f9a-107">Data Type</span></span>

<span data-ttu-id="95f9a-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="95f9a-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="95f9a-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="95f9a-109">Default Value</span></span>

<span data-ttu-id="95f9a-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="95f9a-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="95f9a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95f9a-111">Remarks</span></span>

<span data-ttu-id="95f9a-112">Si esta propiedad tiene un valor de VARIANT \_ false y el resultado es estéreo, el descodificador de audio usa un simple plegado de canal.</span><span class="sxs-lookup"><span data-stu-id="95f9a-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="95f9a-113">Si esta propiedad tiene un valor de VARIANT \_ true, el descodificador de audio realiza Lt-Rt (matriz) en estéreo y, a continuación, se puede usar cualquier descodificador Dolby Surround para descodificar el código envolvente de matriz.</span><span class="sxs-lookup"><span data-stu-id="95f9a-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="95f9a-114">Por ejemplo, el descodificador de audio podría realizar Lt-Rt desplegar en el contenido 5,1 o 7,1.</span><span class="sxs-lookup"><span data-stu-id="95f9a-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="95f9a-115">Esta propiedad solo se admite cuando el descodificador actúa como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="95f9a-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="95f9a-116">No se admite la displiegue de ningún tipo cuando el descodificador actúa como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="95f9a-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="95f9a-117">En Windows Vista, si obtiene una interfaz **IPropertyStore** en un descodificador de audio, el descodificador actúa como MFT.</span><span class="sxs-lookup"><span data-stu-id="95f9a-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="95f9a-118">Por consiguiente, esta propiedad no se puede usar en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="95f9a-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="95f9a-119">Para obtener información sobre cuándo un descodificador actúa como DMO o MFT, consulte las páginas de referencia de códecs individuales en [objetos de códec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="95f9a-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95f9a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f9a-120">Requirements</span></span>



| <span data-ttu-id="95f9a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f9a-121">Requirement</span></span> | <span data-ttu-id="95f9a-122">Value</span><span class="sxs-lookup"><span data-stu-id="95f9a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95f9a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95f9a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95f9a-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="95f9a-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="95f9a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95f9a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95f9a-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="95f9a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95f9a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95f9a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95f9a-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95f9a-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95f9a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="95f9a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f9a-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="95f9a-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
