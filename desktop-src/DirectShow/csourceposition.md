---
description: CSourcePosition es una clase abstracta para implementar la interfaz IMediaPosition en un filtro de origen.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: CSourcePosition (clase)
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
ms.openlocfilehash: 5264bd28e40c8bf20d2c5c514b24d5150eec261a6a25422ff5b1bafc91a13e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687445"
---
# <a name="csourceposition-class"></a>CSourcePosition (clase)

`CSourcePosition` es una clase abstracta para implementar la [**interfaz IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) en un filtro de origen.

Esta clase está obsoleta. Si el filtro de origen es buscable, debe exponer la [**interfaz IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) en lugar de **IMediaPosition**. Puede usar la clase base [**CSourceSeeking**](csourceseeking.md) para este propósito.

 

 



