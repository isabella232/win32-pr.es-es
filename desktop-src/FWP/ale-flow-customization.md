---
title: Personalización de Flow ALE
description: El filtrado de red en las capas de aplicación de cumplimiento de capa de aplicación (ALE) de Windows Filtering Platform (WFP) se puede personalizar agregando filtros con opciones de clasificación específicas.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe42a6df32bc69ba454226eb113cb43756224daaf752c3925f1f2d3bacd7650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951383"
---
# <a name="ale-flow-customization"></a>Personalización de Flow ALE

El filtrado de red en las capas de aplicación de cumplimiento de capa de aplicación (ALE) de Windows Filtering Platform (WFP) se puede personalizar agregando filtros con opciones de clasificación específicas.

## <a name="multicastbroadcast-traffic"></a>Tráfico de multidifusión/difusión

Para bloquear el tráfico entrante en función de los estados de multidifusión o difusión salientes, agregue un filtro que autorice el tráfico de difusión y multidifusión saliente y que tenga la opción [**FWP \_ CLASSIFY OPTION MULTICAST \_ \_ \_ STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) establecida en **FWP OPTION VALUE DENY \_ MULTICAST \_ \_ \_ \_ STATE**.

## <a name="remote-peers"></a>Emparejamientos remotos

Para agregar paquetes de respuesta de distintos elementos del mismo nivel al mismo flujo de ALE, agregue un filtro que tenga la opción [**\_ FWP CLASSIFY \_ OPTION LOOSE \_ SOURCE \_ \_ MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) establecida en **FWP OPTION VALUE ENABLE \_ LOOSE SOURCE \_ \_ \_ \_ \_ MAPPING**.

Vea Using Classify Options for code sample (Uso [de opciones de clasificación](using-classify-options.md) para el ejemplo de código).

## <a name="ale-flow-lifetime"></a>Duración de Flow ALE

Para modificar los valores de tiempo de espera de inactividad de un flujo de ALE, agregue un filtro que tenga la opción [**FWP \_ CLASSIFY OPTION \_ \_ MCAST \_ BCAST \_ LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) o la opción **FWP CLASSIFY OPTION \_ \_ \_ UNICAST \_ LIFETIME** establecida en el valor de tiempo de espera de inactividad deseado.

Consulte [Uso de opciones de clasificación](using-classify-options.md) para obtener un ejemplo de código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de la capa de aplicación (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

[Filtrado con estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfico de multidifusión/difusión de ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorización de ALE](ale-re-authorization.md)
</dt> <dt>

[Usar opciones de clasificación](using-classify-options.md)
</dt> </dl>

 

 




