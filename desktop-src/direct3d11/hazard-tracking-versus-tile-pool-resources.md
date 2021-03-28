---
title: Seguimiento de peligros frente a recursos de grupos de iconos
description: En el caso de los recursos no en mosaico, Direct3D puede evitar ciertas condiciones de riesgo durante la representación, pero como el seguimiento de peligros sería un nivel de mosaico para los recursos en mosaico, el seguimiento de condiciones de riesgo durante la representación de recursos en mosaico podría ser demasiado caro.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418426"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Seguimiento de peligros frente a recursos de grupos de iconos

En el caso de los recursos no en mosaico, Direct3D puede evitar ciertas condiciones de riesgo durante la representación, pero como el seguimiento de peligros sería un nivel de mosaico para los recursos en mosaico, el seguimiento de condiciones de riesgo durante la representación de recursos en mosaico podría ser demasiado caro.

Por ejemplo, en el caso de los recursos no en mosaico, el tiempo de ejecución no permite que se enlace ningún subrecurso dado como entrada (por ejemplo, un ShaderResourceView) y como salida (por ejemplo, un RenderTargetView) al mismo tiempo. Si se encuentra este caso, el tiempo de ejecución desenlaza la entrada. Esta sobrecarga de seguimiento en tiempo de ejecución es barata y se realiza en el nivel de subrecurso. Una de las ventajas de esta sobrecarga de seguimiento es minimizar las posibilidades de que las aplicaciones dependan accidentalmente según el orden de ejecución del sombreador de hardware. El orden de ejecución del sombreador de hardware puede variar si no se trata de una unidad de procesamiento de gráficos (GPU) determinada y, en realidad, de distintas GPU.

El seguimiento de cómo se enlazan los recursos puede ser demasiado caro para los recursos en mosaico porque el seguimiento se encuentra en un nivel de mosaico. Surgen nuevos problemas como, por ejemplo, la validación de los intentos de representación en un RenderTargetView con un mosaico asignado a varias áreas de la superficie simultáneamente. Si este seguimiento de riesgos por mosaico es demasiado caro para el tiempo de ejecución, idealmente esto sería una opción en la capa de depuración.

Una aplicación debe informar al controlador de pantalla cuando se ha emitido una operación de lectura o escritura en un recurso en mosaico que hace referencia a la memoria del grupo de mosaicos al que también se hará referencia mediante recursos en mosaico independientes en las próximas operaciones de lectura o escritura que espera que la primera operación se complete antes de que puedan comenzar las siguientes operaciones. Para obtener más información sobre esta condición, consulte [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) Comentarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




