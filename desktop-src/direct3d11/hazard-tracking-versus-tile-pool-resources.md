---
title: Seguimiento de peligros frente a recursos de grupos de iconos
description: En el caso de los recursos que no están en mosaico, Direct3D puede evitar ciertas condiciones de peligro durante la representación, pero dado que el seguimiento de riesgos se realizaría en un nivel de mosaico para los recursos en mosaico, el seguimiento de las condiciones de peligro durante la representación de los recursos en mosaico podría ser demasiado costoso.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b30feeba564371055ee4297c6795396173a46272f43ffe43af353b17abc0193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952905"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Seguimiento de peligros frente a recursos de grupos de iconos

En el caso de los recursos que no están en mosaico, Direct3D puede evitar ciertas condiciones de peligro durante la representación, pero dado que el seguimiento de riesgos se realizaría en un nivel de mosaico para los recursos en mosaico, el seguimiento de las condiciones de peligro durante la representación de los recursos en mosaico podría ser demasiado costoso.

Por ejemplo, en el caso de los recursos que no están en mosaico, el tiempo de ejecución no permite enlazar ningún subresource determinado como entrada (como ShaderResourceView) y como salida (por ejemplo, RenderTargetView) al mismo tiempo. Si se encuentra un caso de este tipo, el tiempo de ejecución desenlazó la entrada. Esta sobrecarga de seguimiento en tiempo de ejecución es económica y se realiza en el nivel SubResource. Una de las ventajas de esta sobrecarga de seguimiento es minimizar las posibilidades de que las aplicaciones se alojen accidentalmente en función del orden de ejecución del sombreador de hardware. El orden de ejecución del sombreador de hardware puede variar si no se encuentra en una unidad de procesamiento gráfico (GPU) determinada y, por supuesto, en diferentes GPU.

El seguimiento de cómo se enlazan los recursos puede ser demasiado costoso para los recursos en mosaico porque el seguimiento se encuentra en un nivel de mosaico. Surgen nuevos problemas, como la posible validación de los intentos de representación en RenderTargetView con un icono asignado a varias áreas de la superficie simultáneamente. Si resulta que este seguimiento de riesgos por mosaico es demasiado costoso para el tiempo de ejecución, lo ideal sería al menos una opción en la capa de depuración.

Una aplicación debe informar al controlador de pantalla cuando haya emitido una operación de escritura o lectura en un recurso en mosaico que haga referencia a la memoria del grupo de mosaicos a la que también se hará referencia mediante recursos en mosaico independientes en las próximas operaciones de lectura o escritura que espera que se complete la primera operación antes de que puedan comenzar las operaciones siguientes. Para obtener más información sobre esta condición, vea los comentarios [**ID3D11DeviceContext2::TiledResourceBarcontext.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




