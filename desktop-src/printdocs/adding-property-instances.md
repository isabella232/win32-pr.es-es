---
description: Obtenga información sobre cómo agregar instancias de propiedad. El esquema de impresión permite que las instancias de propiedad se presenten en una instancia de Opción.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Agregar instancias de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409698"
---
# <a name="adding-property-instances"></a><span data-ttu-id="1e005-104">Agregar instancias de propiedad</span><span class="sxs-lookup"><span data-stu-id="1e005-104">Adding Property Instances</span></span>

<span data-ttu-id="1e005-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="1e005-105">This topic is not current.</span></span> <span data-ttu-id="1e005-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1e005-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1e005-107">El esquema de impresión permite que las instancias de propiedad se presenten en una instancia de Opción.</span><span class="sxs-lookup"><span data-stu-id="1e005-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="1e005-108">Las instancias de propiedad definidas en el documento PrintCapabilities no se propagan a las instancias option guardadas en PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1e005-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="1e005-109">Los elementos de propiedad no afectan al resultado del proceso de puntuación cuando se comparan dos instancias de Option, pero las instancias scoredProperty afectan a este proceso.</span><span class="sxs-lookup"><span data-stu-id="1e005-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="1e005-110">Todos los controladores de dispositivo que implementan un algoritmo de puntuación deben observar esta convención.</span><span class="sxs-lookup"><span data-stu-id="1e005-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="1e005-111">Los proveedores de PrintCapabilities pueden agregar instancias de propiedad a una opción si estas instancias son específicas de esa opción concreta y ninguna otra, o si el proveedor pretende que el valor de esta propiedad aparezca para cada opción de la característica.</span><span class="sxs-lookup"><span data-stu-id="1e005-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="1e005-112">Por ejemplo, suponga que la propiedad PrintRate depende de la opción seleccionada para la característica PageResolution.</span><span class="sxs-lookup"><span data-stu-id="1e005-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="1e005-113">Si la propiedad PrintRate se colocara en el nivel raíz del documento PrintCapabilities, sería de un solo valor y reflejaría solo la velocidad de impresión de la resolución seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="1e005-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="1e005-114">Sin embargo, si la propiedad PrintRate se colocara dentro de cada opción PageResolution, cada instancia de la propiedad PrintRate podría reflejar la velocidad de impresión de la opción PageResolution que la contenía.</span><span class="sxs-lookup"><span data-stu-id="1e005-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="1e005-115">El documento PrintCapabilities contendrá varias definiciones para PrintRate, una correspondiente a cada opción PageResolution.</span><span class="sxs-lookup"><span data-stu-id="1e005-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="1e005-116">Con una representación abreviada, PrintCapabilities contendrá:</span><span class="sxs-lookup"><span data-stu-id="1e005-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

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

<span data-ttu-id="1e005-117">En algunas situaciones, colocar una propiedad de velocidad de impresión dentro de cada opción de resolución es más conveniente para el cliente, ya que el cliente puede determinar de un vistazo el efecto que tiene cada opción de resolución en la velocidad de impresión, sin necesidad de obtener un nuevo documento PrintCapabilities para cada configuración de resolución.</span><span class="sxs-lookup"><span data-stu-id="1e005-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="1e005-118">Tenga en cuenta también que las instancias de propiedad también se pueden agregar como elementos secundarios de elementos Feature.</span><span class="sxs-lookup"><span data-stu-id="1e005-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="1e005-119">Esto resulta útil si hay instancias de propiedad o valores de instancias de propiedad que son específicos de cada característica.</span><span class="sxs-lookup"><span data-stu-id="1e005-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="1e005-120">Por ejemplo, puede haber una propiedad que especifique si solo se puede seleccionar una opción a la vez para una característica o si se pueden seleccionar varias opciones.</span><span class="sxs-lookup"><span data-stu-id="1e005-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="1e005-121">Esta es la propiedad PICK \_ ONE, PICK \_ MANY que se usa en los archivos PPD y GPD.</span><span class="sxs-lookup"><span data-stu-id="1e005-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="1e005-122">Dado que algunas instancias de característica pueden identificarse como PICK ONE, mientras que otras se podrían identificar como PICK MANY, esta propiedad \_ \_ debe definirse para cada característica.</span><span class="sxs-lookup"><span data-stu-id="1e005-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="1e005-123">Al buscar la propiedad como un elemento secundario de la característica, se produce la asociación entre la propiedad y la característica.</span><span class="sxs-lookup"><span data-stu-id="1e005-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e005-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e005-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e005-125">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1e005-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



