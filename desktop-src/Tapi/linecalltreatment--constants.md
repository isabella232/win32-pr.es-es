---
description: Las \_ constantes LINECALLTREATMENT muestran los tratamientos de las llamadas que no tienen respuesta o están en espera. A excepción de la validación de parámetros básica, el tratamiento de llamadas es un paso directo por TAPI al proveedor de servicios.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Constantes de LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690922"
---
# <a name="linecalltreatment_-constants"></a>Constantes de LINECALLTREATMENT \_

Las **constantes \_ LINECALLTREATMENT** muestran los tratamientos de las llamadas que no tienen respuesta o están en espera. A excepción de la validación de parámetros básica, el tratamiento de llamadas es un paso directo por TAPI al proveedor de servicios.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ ocupado**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha la señal de ocupación.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_música LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha la música.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**\_timbre LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha el tono de timbre.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**silencio de LINECALLTREATMENT \_**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o en suspensión), la parte escucha el silencio.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El valor 0x00000000 está reservado para indicar que el proveedor de servicios no admite los tratamientos de llamadas. Los valores del intervalo de 0x00000005 a 0x000000FF se reservan para una definición futura. Los valores en el intervalo de 0x00000100 a 0xFFFFFFFF están reservados para la asignación por proveedores de servicios y pueden incluir la identificación de selecciones musicales o anuncios grabados específicos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




