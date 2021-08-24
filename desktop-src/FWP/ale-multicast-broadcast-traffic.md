---
title: Tráfico de multidifusión/difusión de ALE
description: Todo el tráfico entrante de multidifusión y difusión en las capas de aplicación de la capa de aplicación (ALE) se asigna a un flujo global de ALE.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2849f7277cc9ada580bca22fa5a4fdf618d959d255b442607963047dd2a37bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315615"
---
# <a name="ale-multicastbroadcast-traffic"></a>Tráfico de multidifusión/difusión de ALE

Todo el tráfico entrante de multidifusión y difusión en las capas de aplicación de la capa de aplicación (ALE) se asigna a un flujo [global de ALE.](ale-stateful-filtering.md) El tráfico de respuesta para los paquetes de multidifusión y difusión entrantes se clasifica en la capa [**FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) y se crean flujos de ALE independientes para cada respuesta.

La multidifusión saliente y el tráfico de difusión en las capas de ALE crean un flujo de ALE de 4 segundos. De forma predeterminada, la autorización de un paquete ALE de difusión o multidifusión saliente permitirá el tráfico entrante, ya sea unidifusión, multidifusión o difusión, desde cualquier dirección remota durante un máximo de 4 segundos. Este flujo de ALE solo se puede actualizar o mantener activo mediante el tráfico saliente posterior que coincida con el flujo de ALE.

> [!Note]  
> La duración de 4 segundos se especifica mediante la llamada integrada [**FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V{4 \| 6}**](built-in-callout-identifiers.md). Para modificar la duración predeterminada de 4 segundos, agregue un filtro que haga referencia a la llamada **FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V{4 \| 6}.** Vea [Personalización de Flow ALE](ale-flow-customization.md) para obtener más información.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de la capa de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalización de Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 




