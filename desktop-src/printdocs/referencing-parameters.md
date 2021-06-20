---
description: Obtenga información sobre cómo hacer referencia a parámetros y el elemento ParameterDef. Un ejemplo de una opción que incluye un elemento ParameterRef es la opción de tamaño de medio personalizado.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Referencia a parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650790af5ca6849bd082b4819dd4c411adea320f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405328"
---
# <a name="referencing-parameters"></a><span data-ttu-id="d61c8-104">Referencia a parámetros</span><span class="sxs-lookup"><span data-stu-id="d61c8-104">Referencing Parameters</span></span>

<span data-ttu-id="d61c8-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d61c8-105">This topic is not current.</span></span> <span data-ttu-id="d61c8-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d61c8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d61c8-107">Un ejemplo concreto de una opción que incluye un elemento ParameterRef es la opción de tamaño de medio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d61c8-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="d61c8-108">Tenga en cuenta que hace referencia a dos parámetros: PageMediaSizeMediaSizeWidth y PageMediaSizeMediaSizeHeight.</span><span class="sxs-lookup"><span data-stu-id="d61c8-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="d61c8-109">Cada instancia de ParameterRef hace referencia a una instancia de ParameterDef que se define en otra parte del documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d61c8-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="d61c8-110">Para obtener información sobre el elemento ParameterDef, vea [ParameterDef](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="d61c8-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="d61c8-111">Para obtener información conceptual sobre cómo definir parámetros, vea [ParameterDef y ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="d61c8-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="d61c8-112">Simplemente crear una opción con parámetros no es suficiente para asegurarse de que la opción se controlará y procesará correctamente.</span><span class="sxs-lookup"><span data-stu-id="d61c8-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="d61c8-113">El proveedor PrintCapabilities/PrintTicket y los clientes deben proporcionar compatibilidad adicional para implementar correctamente instancias option parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="d61c8-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="d61c8-114">Los comportamientos necesarios se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="d61c8-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d61c8-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d61c8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d61c8-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d61c8-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



