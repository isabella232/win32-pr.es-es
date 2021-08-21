---
description: Un TSP usa estas constantes para identificar el tipo de nivel de QoS (calidad de servicio) necesario.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: LINEQOSSERVICELEVEL_ constantes (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a74a4508b54a8b56e8e9cb359f966122c5c009f0e5ede0f1b8544cd1e46330c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003013"
---
# <a name="lineqosservicelevel_-constants"></a>LineQOSSERVICELEVEL \_ (Constantes)

Un TSP usa estas constantes para identificar el tipo de nivel de QoS (calidad de servicio) necesario.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ NEEDED**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



La calidad del nivel de servicio solicitado es un requisito.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



La calidad del nivel de servicio necesaria, si está disponible.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



La calidad del nivel de servicio necesaria es el "mejor esfuerzo".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



 

 




