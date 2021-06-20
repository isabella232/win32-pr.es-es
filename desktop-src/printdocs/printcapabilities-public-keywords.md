---
description: Obtenga información sobre los elementos configurables por el usuario y las definiciones de parámetros que pueden ser aplicables a un documento PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palabras clave públicas de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d836ca13297f031897598bb2ecbfc6588c49753
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407098"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="d3f1e-103">Palabras clave públicas de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="d3f1e-103">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="d3f1e-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-104">This topic is not current.</span></span> <span data-ttu-id="d3f1e-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d3f1e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d3f1e-106">En la sección siguiente se especifican los elementos configurables por el usuario y las definiciones de parámetros que pueden ser aplicables a un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-106">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="d3f1e-107">Uso de elementos configurables por el usuario</span><span class="sxs-lookup"><span data-stu-id="d3f1e-107">User Configurable Elements Usage</span></span>

<span data-ttu-id="d3f1e-108">Los elementos configurables por el usuario representan palabras clave públicas del esquema de impresión que pueden aparecer en un documento PrintCapabilities o printTicket.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-108">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="d3f1e-109">Están diseñados para representar atributos de dispositivo configurables admitidos por un dispositivo específico o comunicar la intención de configuración de impresión por parte de una aplicación o usuario.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-109">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="d3f1e-110">Los elementos configurables por el usuario pueden hacer referencia a elementos de referencia de parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-110">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="d3f1e-111">Para obtener más información, consulte la sección [Elementos de referencia de](parameter-reference-elements.md) parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-111">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="d3f1e-112">Uso de definiciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="d3f1e-112">Parameter Definitions Usage</span></span>

<span data-ttu-id="d3f1e-113">Las definiciones de parámetros tienen la forma de tipos de elemento ParameterDef en un documento De capacidades de impresión.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-113">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="d3f1e-114">Los tipos de elemento ParameterDef se inicializan en printTicket mediante el tipo de elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-114">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="d3f1e-115">El valor del parámetro se especificará mediante el elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-115">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="d3f1e-116">Una palabra clave configurable por el usuario puede hacer referencia a una definición de parámetro mediante el tipo de elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="d3f1e-116">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="d3f1e-117">Para obtener más información, consulte la sección [Construcciones de parámetros.](parameter-constructs.md)</span><span class="sxs-lookup"><span data-stu-id="d3f1e-117">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3f1e-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3f1e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f1e-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d3f1e-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



