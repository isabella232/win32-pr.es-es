---
description: Un TSP usa estas constantes para identificar el tipo de nivel de QoS (calidad de servicio) necesario.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Constantes de LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690750"
---
# <a name="lineqosservicelevel_-constants"></a>Constantes de LINEQOSSERVICELEVEL \_

Un TSP usa estas constantes para identificar el tipo de nivel de QoS (calidad de servicio) necesario.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ necesaria**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



El nivel de calidad de servicio solicitado es un requisito.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



El nivel de calidad de servicio necesario, si está disponible.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



El nivel de calidad de servicio necesario es "mejor esfuerzo".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




