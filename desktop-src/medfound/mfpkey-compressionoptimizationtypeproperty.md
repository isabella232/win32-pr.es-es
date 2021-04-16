---
description: Especifica los valores de calidad visual óptimos que se usarán para el codificador de perfil avanzado de Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Propiedad MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696954"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="5f89e-103">\_Propiedad COMPRESSIONOPTIMIZATIONTYPE de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5f89e-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="5f89e-104">Especifica los valores de calidad visual óptimos que se usarán para el codificador de perfil avanzado de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="5f89e-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5f89e-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5f89e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5f89e-106">g \_ wszWMVCCompressionOptimizationType</span><span class="sxs-lookup"><span data-stu-id="5f89e-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="5f89e-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5f89e-107">Data Type</span></span>

<span data-ttu-id="5f89e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5f89e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5f89e-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="5f89e-109">Default Value</span></span>

<span data-ttu-id="5f89e-110">0</span><span class="sxs-lookup"><span data-stu-id="5f89e-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="5f89e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f89e-111">Remarks</span></span>

<span data-ttu-id="5f89e-112">Esta propiedad proporciona una manera rápida de configurar una serie de opciones de codificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f89e-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="5f89e-113">Se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f89e-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f89e-114">Value</span><span class="sxs-lookup"><span data-stu-id="5f89e-114">Value</span></span></th>
<th><span data-ttu-id="5f89e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f89e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f89e-116">0</span><span class="sxs-lookup"><span data-stu-id="5f89e-116">0</span></span></td>
<td><span data-ttu-id="5f89e-117">El códec no forzará la optimización y usará las características especificadas por otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f89e-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="5f89e-118">En muchos casos, el códec usará la lógica interna para determinar la configuración si no se especifican.</span><span class="sxs-lookup"><span data-stu-id="5f89e-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="5f89e-119">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5f89e-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f89e-120">1</span><span class="sxs-lookup"><span data-stu-id="5f89e-120">1</span></span></td>
<td><span data-ttu-id="5f89e-121">Habilita las características que producirán la mejor calidad visual. Al usar este valor, se configura el códec como si hubiera establecido las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="5f89e-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="5f89e-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="5f89e-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="5f89e-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="5f89e-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="5f89e-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="5f89e-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="5f89e-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="5f89e-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="5f89e-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="5f89e-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="5f89e-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="5f89e-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="5f89e-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="5f89e-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="5f89e-129">Si establece cualquiera de las propiedades de la lista anterior, el valor que establezca invalidará los valores asociados a este valor, a excepción de <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="5f89e-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5f89e-130">Establecer el valor de la \_ propiedad MFPKEY COMPRESSIONOPTIMIZATIONTYPE en 1 también tiene el efecto de establecer el valor del registro de la opción Dquant en 2 y el valor del registro del método de costo del vector de movimiento en 1.</span><span class="sxs-lookup"><span data-stu-id="5f89e-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="5f89e-131">Para obtener más información, vea el artículo Web [uso de la configuración avanzada del códec de perfil avanzado de Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span><span class="sxs-lookup"><span data-stu-id="5f89e-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f89e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f89e-132">Requirements</span></span>



| <span data-ttu-id="5f89e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f89e-133">Requirement</span></span> | <span data-ttu-id="5f89e-134">Value</span><span class="sxs-lookup"><span data-stu-id="5f89e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f89e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f89e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5f89e-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5f89e-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5f89e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f89e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5f89e-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f89e-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f89e-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f89e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f89e-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f89e-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f89e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f89e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f89e-142">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f89e-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




