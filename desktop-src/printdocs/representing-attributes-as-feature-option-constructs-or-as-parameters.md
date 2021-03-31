---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representar atributos como construcciones de características/opciones o como parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083600"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="9772c-104">Representar atributos como construcciones de características/opciones o como parámetros</span><span class="sxs-lookup"><span data-stu-id="9772c-104">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="9772c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="9772c-105">This topic is not current.</span></span> <span data-ttu-id="9772c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9772c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9772c-107">El autor de un documento de PrintCapabilities define los atributos de dispositivo que componen la configuración.</span><span class="sxs-lookup"><span data-stu-id="9772c-107">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="9772c-108">En el documento de PrintCapabilities, el autor puede elegir representar un atributo de dispositivo como una construcción de característica/opción o como una construcción de parámetro.</span><span class="sxs-lookup"><span data-stu-id="9772c-108">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="9772c-109">Si un atributo de dispositivo tiene un número relativamente pequeño de Estados posibles que no entran en ningún tipo de patrón obvio, una construcción de característica/opción suele ser la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="9772c-109">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="9772c-110">Por ejemplo, si los valores permitidos para el atributo de dispositivo PageMediaSize son los valores Letter, legal, A4ISO, tabloide y Envelope10, una construcción de característica/opción sería la mejor opción para la representación.</span><span class="sxs-lookup"><span data-stu-id="9772c-110">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="9772c-111">Debido a la dificultad y la ambigüedad asociadas a la expresión de los valores permitidos sin enumeración explícita, la construcción del parámetro no es adecuada para el atributo PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="9772c-111">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="9772c-112">Si un atributo de dispositivo se puede representar mediante un intervalo de enteros, la representación de los parámetros suele ser la mejor opción, especialmente en el caso de los intervalos que incluyen muchos valores.</span><span class="sxs-lookup"><span data-stu-id="9772c-112">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="9772c-113">Por ejemplo, si el atributo de dispositivo CopyCount para un modelo determinado de impresora puede oscilar entre 1 y 99.999, este atributo se debe clasificar como un parámetro, definiendo una instancia de ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="9772c-113">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="9772c-114">Asigne valores a las instancias de propiedad estándar MinValue y MaxValue del elemento ParameterDef para definir el intervalo de valores para el atributo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="9772c-114">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="9772c-115">Debido al gran número de valores que se deben enumerar explícitamente como elementos de opción, la representación de características y opciones no es adecuada para el atributo de dispositivo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="9772c-115">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9772c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9772c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9772c-117">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9772c-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



