---
description: Representar atributos como construcciones de características o opciones o como parámetros. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representar atributos como construcciones de características o opciones o como parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120060"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="61b8a-105">Representar atributos como construcciones de características o opciones o como parámetros</span><span class="sxs-lookup"><span data-stu-id="61b8a-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="61b8a-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="61b8a-106">This topic is not current.</span></span> <span data-ttu-id="61b8a-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="61b8a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="61b8a-108">El autor de un documento PrintCapabilities define los atributos de dispositivo que la configuración.</span><span class="sxs-lookup"><span data-stu-id="61b8a-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="61b8a-109">En el documento PrintCapabilities, el autor puede elegir representar un atributo de dispositivo como una construcción feature/option o como una construcción de parámetros.</span><span class="sxs-lookup"><span data-stu-id="61b8a-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="61b8a-110">Si un atributo de dispositivo tiene un número relativamente pequeño de estados posibles que no se incluyen en ningún tipo de patrón obvio, una construcción característica/opción suele ser la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="61b8a-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="61b8a-111">Por ejemplo, si los valores permitidos para el atributo de dispositivo PageMediaSize son los valores Letter, Legal, A4ISO, Tabloid y Envelope10, una construcción característica/opción sería la mejor opción para la representación.</span><span class="sxs-lookup"><span data-stu-id="61b8a-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="61b8a-112">Debido a la dificultad y ambigüedad asociadas a expresar los valores permitidos sin enumeración explícita, la construcción de parámetros no es adecuada para el atributo PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="61b8a-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="61b8a-113">Si un atributo de dispositivo se puede representar mediante un intervalo de enteros, la representación de parámetros suele ser la mejor opción, especialmente para los intervalos que incluyen muchos valores.</span><span class="sxs-lookup"><span data-stu-id="61b8a-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="61b8a-114">Por ejemplo, si el atributo de dispositivo CopyCount para un modelo determinado de impresora puede oscilar entre 1 y 99 9999, este atributo debe clasificarse como un parámetro mediante la definición de una instancia parameterDef.</span><span class="sxs-lookup"><span data-stu-id="61b8a-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="61b8a-115">Asigne valores a las instancias de propiedad estándar MinValue y MaxValue del elemento ParameterDef para definir el intervalo de valores para el atributo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="61b8a-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="61b8a-116">Debido al gran número de valores que se deben enumerar explícitamente como elementos Option, la representación Feature/Option no es adecuada para el atributo de dispositivo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="61b8a-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61b8a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61b8a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61b8a-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="61b8a-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



