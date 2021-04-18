---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Referencia a parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707624"
---
# <a name="referencing-parameters"></a><span data-ttu-id="c82ba-104">Referencia a parámetros</span><span class="sxs-lookup"><span data-stu-id="c82ba-104">Referencing Parameters</span></span>

<span data-ttu-id="c82ba-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="c82ba-105">This topic is not current.</span></span> <span data-ttu-id="c82ba-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c82ba-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c82ba-107">Un ejemplo concreto de una opción que incluye un elemento ParameterRef es la opción de tamaño multimedia personalizado.</span><span class="sxs-lookup"><span data-stu-id="c82ba-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="c82ba-108">Tenga en cuenta que hace referencia a dos parámetros: PageMediaSizeMediaSizeWidth y PageMediaSizeMediaSizeHeight.</span><span class="sxs-lookup"><span data-stu-id="c82ba-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="c82ba-109">Cada instancia de ParameterRef hace referencia a una instancia de ParameterDef que se define en otra parte del documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c82ba-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="c82ba-110">Para obtener información sobre el elemento ParameterDef, vea [ParameterDef](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="c82ba-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="c82ba-111">Para obtener información conceptual acerca de la definición de parámetros, vea [elementos ParameterDef y ParameterInit](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="c82ba-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

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

<span data-ttu-id="c82ba-112">Simplemente no basta con crear una opción parametrizada para asegurarse de que la opción se controlará y procesará correctamente.</span><span class="sxs-lookup"><span data-stu-id="c82ba-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="c82ba-113">Los clientes y el proveedor de PrintCapabilities/PrintTicket deben proporcionar compatibilidad adicional para implementar correctamente instancias de opciones con parámetros.</span><span class="sxs-lookup"><span data-stu-id="c82ba-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="c82ba-114">Los comportamientos necesarios se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="c82ba-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c82ba-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c82ba-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c82ba-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c82ba-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



