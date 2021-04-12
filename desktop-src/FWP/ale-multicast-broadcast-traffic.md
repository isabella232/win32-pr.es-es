---
title: Tráfico de multidifusión/difusión ALE
description: Todo el tráfico de multidifusión y difusión entrante en las capas de aplicación de nivel de aplicación (ALE) se asigna a un flujo ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357030"
---
# <a name="ale-multicastbroadcast-traffic"></a>Tráfico de multidifusión/difusión ALE

Todo el tráfico de multidifusión y difusión entrante en las capas de aplicación de nivel de aplicación (ALE) se asigna a un [flujo ALE](ale-stateful-filtering.md)global. El tráfico de respuesta para los paquetes de difusión y multidifusión entrantes se clasifica en el nivel de FWPM de la [**\_ autenticación Ale de capa de \_ \_ \_ conexión \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) y se crean flujos de Ale independientes para cada respuesta.

El tráfico de multidifusión y difusión saliente en los niveles de ALE crea un flujo de ALE de 4 segundos. De forma predeterminada, la autorización de un paquete ALE de multidifusión o de difusión de salida permitirá el tráfico entrante, ya sea unidifusión, multidifusión o difusión, desde cualquier dirección remota durante un máximo de 4 segundos. Este tipo de flujo ALE solo se puede actualizar o mantener activo mediante el siguiente tráfico saliente que coincida con el flujo de ALE.

> [!Note]  
> La duración de 4 segundos se especifica mediante las opciones del conjunto de [**llamada FWPM de llamada integrada \_ \_ \_ OPTION \_ \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md). Para modificar la duración predeterminada de 4 segundos, agregue un filtro que haga referencia a las **\_ Opciones del conjunto de llamadas FWPM \_ \_ \_ auth \_ Connect \_ Layer \_ V {4 \| 6}** CALLOUT. Para obtener más información, consulte [Personalización del flujo ALE](ale-flow-customization.md) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación del nivel de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Niveles ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalización del flujo ALE](ale-flow-customization.md)
</dt> </dl>

 

 




