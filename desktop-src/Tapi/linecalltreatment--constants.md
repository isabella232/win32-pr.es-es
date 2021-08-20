---
description: Las constantes LINECALLTREATMENT enumera los tratamientos para las llamadas sin respuesta \_ o en espera. Excepto para la validación básica de parámetros, el tratamiento de llamadas es un paso directo de TAPI al proveedor de servicios.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: LINECALLTREATMENT_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88c627a89fdf5ab0592c862f09753e0b913eb4b7197a04d4db8cd06478ef10b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863843"
---
# <a name="linecalltreatment_-constants"></a>Constantes LINECALLTREATMENT \_

Las **constantes LINECALLTREATMENT \_** enumera los tratamientos para las llamadas sin respuesta o en espera. Excepto para la validación básica de parámetros, el tratamiento de llamadas es un paso directo de TAPI al proveedor de servicios.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ BUSY**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o entrada), la parte escucha la señal ocupada.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT \_ MUSIC**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o reserva), la parte escucha música.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**ANILLO DE LINECALLTREATMENT \_**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o reserva), la parte escucha el tono de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ SILENCE**
</dt> <dd> <dl> <dt>



Cuando la llamada no está conectada activamente a un dispositivo (oferta o reserva), la parte escucha silencio.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

El valor 0x00000000 reserva para indicar que el proveedor de servicios no admite tratamientos de llamadas. Los valores del intervalo 0x00000005 a 0x000000FF se reservan para futuras definiciones. Los valores del intervalo 0x00000100 a 0xFFFFFFFF están reservados para la asignación por parte de los proveedores de servicios y pueden incluir la identificación de selecciones de música específicas o anuncios grabados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




