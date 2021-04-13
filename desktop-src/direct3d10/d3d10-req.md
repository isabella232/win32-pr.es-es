---
description: Constantes de limitación de recursos.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1d6bf4f72c4ef09eafba3ee50659e5e6ffc682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360053"
---
# <a name="d3d10_req"></a>D3D10 \_ req

Constantes de limitación de recursos.



| \#define                                      | Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Niveles de \_ MIP D3D10 req \_                       | 14    | Número máximo de niveles de mipmap que puede tener un recurso de textura.                                                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ \_ Tamaño de recurso de REQ D3D10 \_ en \_ megabytes     | 128   | Tamaño máximo posible de un recurso en megabytes. Las aplicaciones pueden crear recursos mayores que el tamaño máximo de los recursos en el hardware de gráficos. Sin embargo, se recomienda que las aplicaciones mantengan los recursos más pequeños que el tamaño máximo de los recursos para obtener la máxima compatibilidad entre los proveedores de gráficos. El tiempo de ejecución solo garantiza que las asignaciones dentro del tamaño máximo de los recursos son compatibles con todo el hardware de Direct3D 10. |
| D3D10 \_ req \_ TEXTURE1D \_ \_ dimensión del eje de matriz \_ | 512   | Tamaño máximo de la matriz de una matriz de textura 1D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ req \_ TEXTURE2D \_ \_ dimensión del eje de matriz \_ | 512   | Tamaño máximo de la matriz de una matriz de textura 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ req \_ TEXTURE1D \_ U \_ dimensión           | 8192  | Ancho máximo de una textura 1D.                                                                                                                                                                                                                                                                                                                                                                                                  |
| D3D10 \_ req \_ TEXTURE2D \_ u \_ o \_ V \_ Dimension    | 8192  | Ancho y alto máximo de una textura 2D.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ req \_ TEXTURE3D \_ u \_ V \_ o \_ W \_ Dimension | 2048  | Ancho máximo, alto y profundidad de una textura 3D.                                                                                                                                                                                                                                                                                                                                                                               |
| D3D10 \_ req \_ TEXTURECUBE \_ dimensión            | 8192  | Tamaño máximo de una textura del cubo.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Las constantes se definen en D3D10. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de recursos](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Referencia de Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



