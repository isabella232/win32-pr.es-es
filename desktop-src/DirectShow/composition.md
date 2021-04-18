---
description: Composición
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677075"
---
# <a name="composition"></a>Composición

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El objeto de composición es un contenedor para las pistas. También puede contener otras composiciones (para el anidamiento de pistas), efectos y transiciones. Para crear este objeto, llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .

El objeto de composición expone las siguientes interfaces:

-   [**IAMTimelineComp**](iamtimelinecomp.md)
-   [**IAMTimelineEffectable**](iamtimelineeffectable.md)
-   [**IAMTimelineObj**](iamtimelineobj.md)
-   [**IAMTimelineTransable**](iamtimelinetransable.md)
-   [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de escala de tiempo](the-timeline-model.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



