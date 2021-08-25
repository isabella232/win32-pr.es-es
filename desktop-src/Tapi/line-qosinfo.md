---
description: El mensaje \_ QOSINFO de TSPI LINE hace que TAPI descime un evento qos. Consulte ITQOSEvent para obtener información adicional.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: LINE_QOSINFO mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e6273eb31447f0e0c9543dfa191a25869fa08f05be8a5c639ceb101deff47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873325"
---
# <a name="line_qosinfo-message"></a>Mensaje \_ QOSINFO DE LÍNEA

El mensaje **\_ QOSINFO de TSPI LINE** hace que TAPI descime un evento qos. Consulte [**ITQOSEvent para**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) obtener información adicional.


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

Identificador tapi de la línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Identificador tapi de la llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

El valor LINE \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Miembro del [**enumerador DE EVENTOS \_ de QOS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) que identifica el tipo de evento.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Constante [de tipo de](./tapiprotocol--constants.md) medio que identifica los medios de la llamada asociada a este evento.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EVENTO \_ QOS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

