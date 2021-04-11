---
description: Define valores que especifican las propiedades de una alternativa de reconocimiento. La interfaz de programación de aplicaciones (API) de Tablet PC utiliza identificadores únicos globales (GUID) para identificar las propiedades de los paquetes, que en automatización son cadenas constantes.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Constantes RecognitionProperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361326"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="40939-104">Constantes de RecognitionProperty</span><span class="sxs-lookup"><span data-stu-id="40939-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="40939-105">Define valores que especifican las propiedades de una alternativa de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="40939-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="40939-106">La interfaz de programación de aplicaciones (API) de Tablet PC utiliza identificadores únicos globales (GUID) para identificar las propiedades de los paquetes, que en automatización son cadenas constantes.</span><span class="sxs-lookup"><span data-stu-id="40939-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="40939-107">En la tabla siguiente se enumeran los campos de identificador único global (GUID) de propiedad de reconocimiento disponible.</span><span class="sxs-lookup"><span data-stu-id="40939-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="40939-108">Utilice estos GUID para tener acceso a las propiedades de un objeto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) llamando al método [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .</span><span class="sxs-lookup"><span data-stu-id="40939-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="40939-109">Nombre constante</span><span class="sxs-lookup"><span data-stu-id="40939-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="40939-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40939-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="40939-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-112">GUID que identifica la propiedad del número de línea del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="40939-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="40939-113">LineNumber especifica las alternativas con un número de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="40939-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40939-114">Este campo no se admite para los reconocedores de caracteres de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="40939-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="40939-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-116">GUID que identifica la propiedad para la segmentación del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="40939-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="40939-117">La segmentación especifica el fragmento de tinta básico o la unidad que el reconocedor utiliza para generar un resultado de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="40939-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40939-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="40939-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="40939-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-120">GUID que identifica la propiedad para el punto de conexión de reconocimiento del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="40939-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="40939-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-122">GUID que identifica la propiedad para el recuento máximo de trazos del resultado de reconocimiento del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="40939-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40939-123">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="40939-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="40939-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-125">GUID que identifica la propiedad de la métrica de puntos por pulgada del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="40939-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40939-126">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="40939-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="40939-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-128">GUID que identifica la propiedad para el nivel de confianza que el reconocedor tiene en el resultado del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="40939-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="40939-129">La evaluación de confianza solo está disponible para Estados Unidos inglés y para todos los reconocedores de gestos en Microsoft Windows XP Tablet PC Edition y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="40939-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="40939-130">Los métodos que proporcionan la propiedad Confidence para cualquier otro reconocedor devuelven E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="40939-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="40939-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="40939-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40939-132">GUID que identifica la propiedad de las métricas de línea del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , que es la línea para la que se van a recuperar las métricas.</span><span class="sxs-lookup"><span data-stu-id="40939-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="40939-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40939-133">Remarks</span></span>

<span data-ttu-id="40939-134">En C++, puede tener acceso a estas constantes en el archivo de encabezado Msinkaut. h, que se encuentra en <systemdrive> el \\ Directorio: archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include Si instaló el SDK en la ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40939-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="40939-135">En C++, estas constantes son WCHARs, no BSTR.</span><span class="sxs-lookup"><span data-stu-id="40939-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="40939-136">Conviértalos en BSTR antes de usarlo.</span><span class="sxs-lookup"><span data-stu-id="40939-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="40939-137">Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="40939-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="40939-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40939-138">Requirements</span></span>



| <span data-ttu-id="40939-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="40939-139">Requirement</span></span> | <span data-ttu-id="40939-140">Value</span><span class="sxs-lookup"><span data-stu-id="40939-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40939-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40939-141">Minimum supported client</span></span><br/> | <span data-ttu-id="40939-142">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="40939-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="40939-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40939-143">Minimum supported server</span></span><br/> | <span data-ttu-id="40939-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="40939-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="40939-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40939-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="40939-146"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="40939-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40939-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="40939-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40939-148">**Método AlternatesWithConstantPropertyValues**</span><span class="sxs-lookup"><span data-stu-id="40939-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="40939-149">**Propiedad ConfidenceAlternates**</span><span class="sxs-lookup"><span data-stu-id="40939-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="40939-150">**Propiedad LineAlternates**</span><span class="sxs-lookup"><span data-stu-id="40939-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="40939-151">**Interfaz IInkRecognitionAlternates**</span><span class="sxs-lookup"><span data-stu-id="40939-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




