---
description: Comprenda los parámetros del documento PrintCapabilities. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parámetros del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118630"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="c1162-105">Parámetros del documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c1162-105">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="c1162-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="c1162-106">This topic is not current.</span></span> <span data-ttu-id="c1162-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c1162-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1162-108">Como se describe en [Elementos](parameter-reference-elements.md)de referencia de parámetros , se puede hacer referencia a los elementos ParameterInit desde instancias de Option, pero la construcción de parámetros también tiene un uso que es independiente de este tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="c1162-108">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="c1162-109">Un ejemplo de un atributo de configuración de dispositivo que es adecuado para la representación de parámetros es CopyCount.</span><span class="sxs-lookup"><span data-stu-id="c1162-109">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="c1162-110">Los valores permitidos para este atributo de configuración de dispositivo se pueden definir de forma fácil y concisa sin enumerar cada uno de ellos explícitamente.</span><span class="sxs-lookup"><span data-stu-id="c1162-110">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="c1162-111">Aunque sería posible, aunque tedioso, enumerar cada valor copyCount en su propia opción, algunos atributos de configuración de dispositivo simplemente no se pueden representar mediante una construcción de característica o opción.</span><span class="sxs-lookup"><span data-stu-id="c1162-111">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="c1162-112">Por ejemplo, considere un dispositivo que acepta una cadena de texto que luego se usa para generar una marca de agua virtual en cada página de salida.</span><span class="sxs-lookup"><span data-stu-id="c1162-112">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="c1162-113">El conjunto de todas las cadenas de texto posibles no se puede enumerar explícitamente fácilmente, pero la cadena de texto se puede describir fácilmente mediante un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="c1162-113">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="c1162-114">El documento Palabras clave de esquema de impresión define una serie de construcciones de parámetros usadas con frecuencia, pero los proveedores printCapabilities pueden definir otras adicionales propias.</span><span class="sxs-lookup"><span data-stu-id="c1162-114">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="c1162-115">Sin embargo, estas construcciones de parámetros definidas de forma privada no son portátiles para otros dispositivos, debido al hecho de que un documento PrintCapabilities proporcionado por otra parte no define dicha construcción de parámetro.</span><span class="sxs-lookup"><span data-stu-id="c1162-115">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="c1162-116">Ya sea definido por el esquema o definido de forma privada, la instancia de ParameterDef debe estar presente en el documento PrintCapabilities antes de que los clientes reconozcan y usen el parámetro.</span><span class="sxs-lookup"><span data-stu-id="c1162-116">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="c1162-117">Estos parámetros se conocen como *parámetros designados.*</span><span class="sxs-lookup"><span data-stu-id="c1162-117">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1162-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1162-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1162-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c1162-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



