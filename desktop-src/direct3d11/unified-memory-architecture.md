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
# <a name="unified-memory-architecture"></a>Arquitectura de memoria unificada

La consulta de si se admite la arquitectura de memoria unificada (UMA) puede ayudar a determinar cómo administrar algunos recursos.

Se puede leer un valor booleano, establecido por el controlador, de la estructura de [**D3D11 de \_ datos de características de \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) para determinar si el hardware admite la UMA.

Las aplicaciones que se ejecutan en UMA pueden querer tener más recursos habilitados para el acceso a la CPU que si no están disponibles. UMA permite a las aplicaciones evitar copiar los datos de recursos, en lugar de ser eficientes únicamente para los adaptadores de gráficos no UMA. [Características de Direct3D 11,3](direct3d-11-3-features.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




