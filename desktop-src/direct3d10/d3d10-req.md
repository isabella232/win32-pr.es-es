---
description: Constantes de limitación de recursos.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e099c26706772bbb76ad6709759fa4712e22ea3bc9793b905a2050f25d0f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100757"
---
# <a name="d3d10_req"></a>D3D10 \_ REQ

Constantes de limitación de recursos.



| \#Definir                                      | Valor | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ REQ \_ MIP \_ LEVELS                       | 14    | Número máximo de niveles de mapa mip que puede tener un recurso de textura.                                                                                                                                                                                                                                                                                                                                                                    |
| TAMAÑO DE RECURSO DE D3D10 \_ REQ \_ EN \_ \_ \_ MEGABYTES     | 128   | Tamaño máximo posible de un recurso en megabytes. Las aplicaciones pueden crear recursos mayores que el tamaño máximo de recursos en algún hardware gráfico. Sin embargo, se recomienda que las aplicaciones mantengan los recursos más pequeños que el tamaño máximo de recursos para obtener la cantidad máxima de compatibilidad entre los proveedores de gráficos. El tiempo de ejecución solo garantiza que todo el hardware de Direct3D 10 admite las asignaciones dentro del tamaño máximo de recursos. |
| D3D10 \_ REQ \_ TEXTURE1D \_ ARRAY \_ AXIS \_ DIMENSION | 512   | Tamaño máximo de matriz de una matriz de textura 1D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ REQ \_ TEXTURE2D \_ ARRAY \_ AXIS \_ DIMENSION | 512   | Tamaño máximo de matriz de una matriz de textura 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ REQ \_ TEXTURE1D \_ U \_ DIMENSION           | 8192  | Ancho máximo de una textura 1D.                                                                                                                                                                                                                                                                                                                                                                                                  |
| D3D10 \_ REQ \_ TEXTURE2D \_ U \_ OR \_ V \_ DIMENSION    | 8192  | Ancho y alto máximos de una textura 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ REQ \_ TEXTURE3D \_ U V O W \_ \_ \_ \_ DIMENSION | 2048  | Ancho, alto y profundidad máximos de una textura 3D.                                                                                                                                                                                                                                                                                                                                                                               |
| D3D10 \_ REQ \_ TEXTURECUBE \_ DIMENSION            | 8192  | Tamaño máximo de una textura de cubo.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Las constantes se definen en D3D10.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de recursos](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Referencia de Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



