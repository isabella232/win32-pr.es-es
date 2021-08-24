---
title: BITS_COST_STATE (Bits5 \_ 0.h)
description: La \_ enumeración BITS COST STATE define los valores constantes que especifican el estado de costo de \_ BITS.
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
ms.openlocfilehash: ecbe54966a54310af71a4c96a3d3c2423f524f9b8a8067b10350fba05675a54b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701985"
---
# <a name="bits_cost_state"></a>ESTADO \_ DE COSTO DE \_ BITS

Define constantes que especifican el estado de costo de BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**BITS \_ COST \_ STATE \_ UNRESTRICTED**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**BITS \_ COST \_ STATE \_ CAPPED \_ USAGE \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**BITS \_ COST \_ STATE \_ BELOW \_ CAP**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**BITS \_ COST \_ STATE \_ NEAR \_ CAP**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**BITS \_ COST \_ STATE \_ OVERCAP \_ CHARGED**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**BITS \_ COST \_ STATE \_ USAGE \_ BASED**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**OPCIÓN BITS \_ COST \_ IGNORE \_ \_ CONGESTION**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**BITS \_ COST \_ STATE \_ RESERVED**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ NOT \_ ROAMING**
</dt> <dd> <dl> <dt>

(BITS) \_ OPCIÓN COST IGNORE CONGESTION BITS COST STATE USAGE BASED BITS COST STATE OVERCAP THROTTLED BITS COST STATE OVERCAP CHARGED BITS COST STATE NEAR CAP BITS COST STATE BELOW CAP BITS COST STATE \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ CAPPED \_ USAGE UNKNOWN BITS COST STATE \_ \| \_ \_ \_ UNRESTRICTED) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ NO \_ SURCHARGE**
</dt> <dd> <dl> <dt>

(BITS) \_ OPCIÓN COST IGNORE CONGESTION BITS COST STATE USAGE BASED BITS COST STATE OVERCAP THROTTLED BITS COST STATE NEAR CAP BITS COST STATE BELOW CAP BITS COST \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ STATE \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ CAPPED USAGE UNKNOWN \_ BITS COST STATE \_ \| \_ \_ \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ STANDARD**
</dt> <dd> <dl> <dt>

(BITS) \_ OPCIÓN COST IGNORE CONGESTION BITS COST \_ STATE USAGE BASED BITS \_ COST \_ STATE \| \_ \_ \_ \_ \| \_ \_ \_ OVERCAP THROTTLED BITS COST STATE BELOW CAP \_ BITS COST \| STATE \_ \_ \_ \_ \| \_ \_ \_ CAPPED USAGE UNKNOWN BITS \_ COST STATE \_ \| \_ \_ \_ UNRESTRICTED) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ UNRESTRICTED**
</dt> <dd> <dl> <dt>

(BITS) \_ OPCIÓN COST \_ IGNORE CONGESTION BITS COST STATE \_ \_ \| \_ \_ \_ OVERCAP \_ THROTTLED BITS COST STATE \| \_ \_ \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ ALWAYS**
</dt> <dd> <dl> <dt>

(BITS) \_ OPCIÓN COST IGNORE CONGESTION BITS COST STATE ROAMING BITS COST STATE USAGE BASED BITS COST COST STATE OVERCAP THROTTLED BITS COST STATE OVERCAP CHARGED BITS COST STATE NEAR CAP BITS COST STATE BELOW CAP BITS COST STATE CAP \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ BITS \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ CAPPED USAGE UNKNOWN \_ BITS COST STATE \_ \| \_ \_ \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Bits5 \_ 0.h (incluir Bits.h)</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Bits5 \_ 0.idl</dt> </dl>                |



 

 





