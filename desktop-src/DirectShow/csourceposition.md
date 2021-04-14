---
description: CSourcePosition es una clase abstracta para implementar la interfaz IMediaPosition en un filtro de origen.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Clase CSourcePosition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659263"
---
# <a name="csourceposition-class"></a>Clase CSourcePosition

`CSourcePosition` es una clase abstracta para implementar la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) en un filtro de origen.

Esta clase está obsoleta. Si el filtro de origen es buscable, debe exponer la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) en lugar de **IMediaPosition**. Puede usar la clase base [**CSourceSeeking**](csourceseeking.md) para este propósito.

 

 



