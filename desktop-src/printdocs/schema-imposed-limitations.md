---
description: Obtenga información sobre las limitaciones impuestas por el esquema PrintCapabilities. El proveedor PrintCapabilities debe detectar configuraciones no válidas y resolverlas.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404928"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="b990f-104">Schema-Imposed limitaciones</span><span class="sxs-lookup"><span data-stu-id="b990f-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="b990f-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="b990f-105">This topic is not current.</span></span> <span data-ttu-id="b990f-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b990f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b990f-107">El esquema PrintCapabilities proporciona a los autores de PrintCapabilities una gran cantidad de flexibilidad y expresividad que se pueden usar en las descripciones de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b990f-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="b990f-108">Sin embargo, las dependencias de configuración imponen una limitación a esta flexibilidad y expresividad.</span><span class="sxs-lookup"><span data-stu-id="b990f-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="b990f-109">Las instancias de ParameterDef, la lista de elementos Feature, la lista de instancias option dentro de cada característica y las instancias scoredProperty dentro de cada opción no deben contener dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="b990f-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="b990f-110">El proveedor de documentos PrintCapabilities debe detectar combinaciones de configuraciones no válidas y debe resolverlas.</span><span class="sxs-lookup"><span data-stu-id="b990f-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b990f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b990f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b990f-112">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b990f-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



