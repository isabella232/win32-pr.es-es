---
title: BITS_COST_STATE (Bits5 \_ 0. h)
description: La \_ enumeración de estado de costo de bits \_ define los valores constantes que especifican el estado de costo de bits.
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: 88fb0b949fb06a6e1eb6e14cdf55c8d54d9ab33c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996510"
---
# <a name="bits_cost_state"></a>\_Estado de costo de bits \_

Define constantes que especifican el estado del costo de BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**Estado de costo de BITS \_ \_ sin \_ restricciones**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**uso límite de estado de costo de BITS \_ \_ \_ \_ \_ desconocido**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**Estado de costo de BITS \_ \_ \_ por debajo del \_ límite**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**Estado de costo de BITS \_ \_ \_ Near \_ Cap**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**Estado de costo de BITS \_ \_ \_ OVERCAP \_ cargado**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**Estado de costo de BITS \_ \_ \_ OVERCAP \_ limitado**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**\_ \_ \_ basado en el uso de estado de costo de bits \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**opción de costo de BITS \_ \_ \_ omitir \_ congestión**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**Estado de costo de BITS \_ \_ \_ reservado**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**transferencia de estado de costo de BITS \_ \_ \_ \_ no \_ móvil**
</dt> <dd> <dl> <dt>

(BITS \_ opción de costo \_ \_ omitir \_ bits de congestión \| \_ costo \_ basado en el uso de estado bits costo OVERCAP bits limitado estado de bits limitados estado OVERCAP de bits de \_ carga aproximado estado de bits de \_ Cap estado por debajo \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ del límite bits de Cap estado límite de uso límite bits desconocido estado de costo no restringido) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**transferencia de estado de costo de BITS \_ \_ \_ \_ sin \_ recargo**
</dt> <dd> <dl> <dt>

(BITS \_ opción de costo \_ \_ omitir \_ bits de congestión \| \_ costo \_ basado en el uso de estado bits basado en el costo OVERCAP bits limitado estado del costo de bits \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ aproximado estado de bits por \_ debajo \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ del límite bits de Cap estado límite de uso límite bits desconocido estado de costo sin restricción)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**\_estándar de \_ transferencia de estado de costo de bits \_ \_**
</dt> <dd> <dl> <dt>

(BITS \_ opción de costo \_ \_ omitir \_ bits de congestión \| \_ costo \_ basado en el uso de estado bits basado en el costo \_ OVERCAP bits limitado estado del \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ costo de bits límite de bits de Cap estado límite de uso limitado bits desconocido estado de costo no restringido) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**transferencia de estado de costo de BITS \_ \_ \_ \_ sin restricciones**
</dt> <dd> <dl> <dt>

(BITS \_ opción de costo \_ \_ omitir \_ bits de congestión \| \_ \_ Estado costo \_ OVERCAP \_ \| bits limitado estado de costo no \_ \_ \_ restringido)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**transferencia de estado de costo de BITS \_ \_ \_ \_ siempre**
</dt> <dd> <dl> <dt>

(BITS \_ opción de costo omitir bits de congestión estado de costo de bits móvil de costo de bits basado en el uso de estado bits de estado OVERCAP de costo de bits limitado de estado OVERCAP de bits de carga de costo aproximado de bits de Cap estado de costo \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ por debajo \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ del límite de estado de costo límite de uso límite de bits desconocido de costo
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Bits5 \_ 0. h (incluye bits. h)</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Bits5 \_ 0. idl</dt> </dl>                |



 

 





