---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palabras clave públicas de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670095"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="9a5c1-104">Palabras clave públicas de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="9a5c1-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="9a5c1-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-105">This topic is not current.</span></span> <span data-ttu-id="9a5c1-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9a5c1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9a5c1-107">En la sección siguiente se especifican los elementos configurables por el usuario y las definiciones de parámetros que pueden ser aplicables a un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="9a5c1-108">Uso de elementos configurables por el usuario</span><span class="sxs-lookup"><span data-stu-id="9a5c1-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="9a5c1-109">Los elementos configurables por el usuario representan palabras clave públicas del esquema de impresión que pueden aparecer en un documento de PrintCapabilities o en un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="9a5c1-110">Están pensadas para representar atributos de dispositivo configurables admitidos por un dispositivo específico o comunicar el intento de impresión por parte de una aplicación o un usuario.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="9a5c1-111">Los elementos configurables por el usuario pueden hacer referencia a elementos de referencia de parámetro.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="9a5c1-112">Para obtener más información, consulte la sección [elementos de referencia de parámetros](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="9a5c1-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="9a5c1-113">Uso de definiciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="9a5c1-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="9a5c1-114">Las definiciones de parámetros adoptan la forma de tipos de elementos ParameterDef en un documento de capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="9a5c1-115">Los tipos de elementos ParameterDef se inicializan en un PrintTicket mediante el tipo de elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="9a5c1-116">El valor del parámetro se especificará mediante el elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="9a5c1-117">Una palabra clave configurable por el usuario puede hacer referencia a una definición de parámetro mediante el tipo de elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="9a5c1-118">Para obtener más información, consulte la sección [construcciones de parámetros](parameter-constructs.md) .</span><span class="sxs-lookup"><span data-stu-id="9a5c1-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a5c1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a5c1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5c1-120">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9a5c1-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



