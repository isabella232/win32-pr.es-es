---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parámetros del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361965"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="90f0a-104">Parámetros del documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="90f0a-104">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="90f0a-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="90f0a-105">This topic is not current.</span></span> <span data-ttu-id="90f0a-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="90f0a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="90f0a-107">Como se describe en [elementos de referencia de parámetros](parameter-reference-elements.md), se puede hacer referencia a los elementos ParameterInit desde instancias de opciones, pero la construcción de parámetro también tiene un uso que es independiente de este tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="90f0a-107">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="90f0a-108">Un ejemplo de un atributo de configuración de dispositivo que está bien adaptado para la representación de parámetros es CopyCount.</span><span class="sxs-lookup"><span data-stu-id="90f0a-108">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="90f0a-109">Los valores permitidos para este atributo de configuración de dispositivo pueden definirse de manera fácil y concisa sin enumerarlos explícitamente.</span><span class="sxs-lookup"><span data-stu-id="90f0a-109">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="90f0a-110">Aunque sería posible, aunque tedioso, mostrar cada valor de CopyCount en su propia opción, algunos atributos de configuración de dispositivos simplemente no se pueden representar mediante una construcción de característica/opción.</span><span class="sxs-lookup"><span data-stu-id="90f0a-110">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="90f0a-111">Por ejemplo, Imagine un dispositivo que acepta una cadena de texto que se usa para generar una marca de agua virtual en cada página de salida.</span><span class="sxs-lookup"><span data-stu-id="90f0a-111">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="90f0a-112">El conjunto de todas las cadenas de texto posibles no se puede enumerar de forma explícita, pero la cadena de texto se puede describir fácilmente mediante un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="90f0a-112">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="90f0a-113">En el documento imprimir palabras clave del esquema se define una serie de construcciones de parámetros de uso frecuente, pero los proveedores de PrintCapabilities son libres para definir otras propias.</span><span class="sxs-lookup"><span data-stu-id="90f0a-113">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="90f0a-114">Sin embargo, estas construcciones de parámetros definidas de forma privada no son portables a otros dispositivos, debido al hecho de que un documento de PrintCapabilities proporcionado por otra parte no define este tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="90f0a-114">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="90f0a-115">Tanto si está definido por el esquema como si está definido de forma privada, la instancia de ParameterDef debe estar presente en el documento de PrintCapabilities antes de que los clientes reconocen y utilicen el parámetro.</span><span class="sxs-lookup"><span data-stu-id="90f0a-115">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="90f0a-116">Estos parámetros se conocen como *parámetros designados*.</span><span class="sxs-lookup"><span data-stu-id="90f0a-116">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90f0a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90f0a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90f0a-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="90f0a-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



