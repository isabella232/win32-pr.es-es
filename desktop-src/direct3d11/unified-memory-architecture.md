---
title: Arquitectura de memoria unificada
description: La consulta de si se admite la arquitectura de memoria unificada (UMA) puede ayudar a determinar cómo administrar algunos recursos.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993979"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="b5e25-103">Arquitectura de memoria unificada</span><span class="sxs-lookup"><span data-stu-id="b5e25-103">Unified Memory Architecture</span></span>

<span data-ttu-id="b5e25-104">La consulta de si se admite la arquitectura de memoria unificada (UMA) puede ayudar a determinar cómo administrar algunos recursos.</span><span class="sxs-lookup"><span data-stu-id="b5e25-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="b5e25-105">Se puede leer un valor booleano, establecido por el controlador, de la estructura de [**D3D11 de \_ datos de características de \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) para determinar si el hardware admite la UMA.</span><span class="sxs-lookup"><span data-stu-id="b5e25-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="b5e25-106">Las aplicaciones que se ejecutan en UMA pueden querer tener más recursos habilitados para el acceso a la CPU que si no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b5e25-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="b5e25-107">UMA permite a las aplicaciones evitar copiar los datos de recursos, en lugar de ser eficientes únicamente para los adaptadores de gráficos no UMA.</span><span class="sxs-lookup"><span data-stu-id="b5e25-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="b5e25-108">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="b5e25-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="b5e25-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5e25-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e25-110">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="b5e25-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




