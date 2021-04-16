---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Agregar instancias de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424143"
---
# <a name="adding-property-instances"></a><span data-ttu-id="1fd47-104">Agregar instancias de propiedad</span><span class="sxs-lookup"><span data-stu-id="1fd47-104">Adding Property Instances</span></span>

<span data-ttu-id="1fd47-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="1fd47-105">This topic is not current.</span></span> <span data-ttu-id="1fd47-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1fd47-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1fd47-107">El esquema de impresión permite que las instancias de la propiedad estén presentes en una instancia de opción.</span><span class="sxs-lookup"><span data-stu-id="1fd47-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="1fd47-108">Las instancias de propiedad definidas en el documento de PrintCapabilities no se propagan a las instancias de opción guardadas en el PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1fd47-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="1fd47-109">Los elementos de propiedad no afectan al resultado del proceso de puntuación cuando se comparan dos instancias de opción, pero las instancias de ScoredProperty afectan a este proceso.</span><span class="sxs-lookup"><span data-stu-id="1fd47-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="1fd47-110">Todos los controladores de dispositivos que implementan un algoritmo de puntuación deben observar esta Convención.</span><span class="sxs-lookup"><span data-stu-id="1fd47-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="1fd47-111">Los proveedores de PrintCapabilities pueden agregar instancias de propiedad a una opción si estas instancias son específicas de esa opción concreta y no otras, o si el proveedor intenta que aparezca el valor de esta propiedad para cada opción de la característica.</span><span class="sxs-lookup"><span data-stu-id="1fd47-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="1fd47-112">Por ejemplo, supongamos que la propiedad PrintRate depende de la opción seleccionada para la característica PageResolution.</span><span class="sxs-lookup"><span data-stu-id="1fd47-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="1fd47-113">Si la propiedad PrintRate se colocó en el nivel raíz del documento de PrintCapabilities, tendría un solo valor y reflejaría solo la tasa de impresión para la resolución seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="1fd47-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="1fd47-114">Sin embargo, si la propiedad PrintRate se colocó dentro de cada opción PageResolution, cada instancia de la propiedad PrintRate podría reflejar la tasa de impresión de la opción PageResolution que la contenía.</span><span class="sxs-lookup"><span data-stu-id="1fd47-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="1fd47-115">El documento PrintCapabilities incluiría varias definiciones para PrintRate, una correspondiente a cada opción PageResolution.</span><span class="sxs-lookup"><span data-stu-id="1fd47-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="1fd47-116">Con una representación abreviada, la PrintCapabilities contendría:</span><span class="sxs-lookup"><span data-stu-id="1fd47-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="1fd47-117">En algunas situaciones, la colocación de una propiedad de velocidad de impresión dentro de cada opción de resolución es más conveniente para el cliente, ya que el cliente puede determinar de un vistazo el efecto que tiene cada opción de resolución en la tasa de impresión, sin necesidad de obtener un nuevo documento de PrintCapabilities para cada configuración de resolución.</span><span class="sxs-lookup"><span data-stu-id="1fd47-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="1fd47-118">Tenga en cuenta también que las instancias de propiedad también se pueden agregar como elementos secundarios de los elementos de característica.</span><span class="sxs-lookup"><span data-stu-id="1fd47-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="1fd47-119">Esto resulta útil si hay instancias de propiedad o valores de instancias de propiedad que son específicos de cada característica.</span><span class="sxs-lookup"><span data-stu-id="1fd47-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="1fd47-120">Por ejemplo, puede haber una propiedad que especifique si solo se permite seleccionar una opción al mismo tiempo para una característica o si se pueden seleccionar varias opciones.</span><span class="sxs-lookup"><span data-stu-id="1fd47-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="1fd47-121">Este es el PICKing \_ , seleccione \_ muchas propiedades que se usan en los archivos PPD y GPD.</span><span class="sxs-lookup"><span data-stu-id="1fd47-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="1fd47-122">Dado que es posible que algunas instancias de características se identifiquen como seleccione \_ una, mientras que otras podrían identificarse como picking \_ many, esta propiedad debe definirse para cada característica.</span><span class="sxs-lookup"><span data-stu-id="1fd47-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="1fd47-123">La búsqueda de la propiedad como un elemento secundario de la característica produce la asociación entre la propiedad y la característica.</span><span class="sxs-lookup"><span data-stu-id="1fd47-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd47-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fd47-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd47-125">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1fd47-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



