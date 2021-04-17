---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitaciones de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698028"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="e9634-104">Limitaciones de Schema-Imposed</span><span class="sxs-lookup"><span data-stu-id="e9634-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="e9634-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="e9634-105">This topic is not current.</span></span> <span data-ttu-id="e9634-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e9634-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e9634-107">El esquema de PrintCapabilities proporciona a los autores de PrintCapabilities una cantidad considerable de flexibilidad y expresividad que se puede usar en las descripciones de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e9634-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="e9634-108">Sin embargo, las dependencias de configuración imponen una limitación en esta flexibilidad y expresividad.</span><span class="sxs-lookup"><span data-stu-id="e9634-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="e9634-109">Las instancias de ParameterDef, la lista de elementos de característica, la lista de instancias de opción dentro de cada característica y las instancias de ScoredProperty dentro de cada opción no deben contener dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="e9634-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="e9634-110">El proveedor de documentos de PrintCapabilities debe detectar combinaciones no válidas de configuraciones y debe resolverlas.</span><span class="sxs-lookup"><span data-stu-id="e9634-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9634-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9634-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9634-112">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="e9634-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



