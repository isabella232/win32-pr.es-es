---
title: Personalización del flujo ALE
description: El filtrado de red en las capas de cumplimiento de capa de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) se puede personalizar agregando filtros con opciones de clasificación específicas.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104358717"
---
# <a name="ale-flow-customization"></a>Personalización del flujo ALE

El filtrado de red en las capas de cumplimiento de capa de aplicación (ALE) de la plataforma de filtrado de Windows (WFP) se puede personalizar agregando filtros con opciones de clasificación específicas.

## <a name="multicastbroadcast-traffic"></a>Tráfico de multidifusión/difusión

Para bloquear el tráfico entrante en función de los Estados de multidifusión o difusión salientes, agregue un filtro que autorice el tráfico de difusión y multidifusión saliente y que tenga la opción de [**\_ \_ \_ \_ Estado de multidifusión Option reclasificación de FWP**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) establecida en el valor de la **\_ opción FWP \_ \_ denegar el \_ \_ Estado de multidifusión**.

## <a name="remote-peers"></a>Homólogos remotos

Para agregar paquetes de respuesta de diferentes elementos del mismo nivel al mismo flujo de ALE, agregue un filtro que tenga la opción de [**\_ \_ \_ \_ \_ asignación de código flexible**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) de la opción de clasificación de FWP establecida en el valor de la opción de **FWP \_ \_ \_ habilitar \_ \_ \_ asignación de origen flexible**.

Vea [usar opciones de clasificación](using-classify-options.md) para el ejemplo de código.

## <a name="ale-flow-lifetime"></a>Duración del flujo de ALE

Para modificar los valores de tiempo de espera de inactividad de un flujo ALE, agregue un filtro que tenga la opción de [**\_ \_ duración de \_ MCAST \_ BCAST \_ de FWP**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) y/o la opción de duración de **\_ \_ \_ unidifusión \_** de la opción de clasificación de FWP establecida en el valor de tiempo de espera de inactividad deseado.

Vea [usar las opciones de clasificación](using-classify-options.md) para obtener un ejemplo de código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación del nivel de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Niveles ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Usar opciones de clasificación](using-classify-options.md)
</dt> </dl>

 

 




