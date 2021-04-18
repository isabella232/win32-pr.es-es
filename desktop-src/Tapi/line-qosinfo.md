---
description: El mensaje QOSINFO de la línea de TSPI \_ hace que TAPI desencadene un evento de QoS. Consulte ITQOSEvent para obtener información adicional.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Mensaje de LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680365"
---
# <a name="line_qosinfo-message"></a>Mensaje de línea \_ QOSINFO

El mensaje **\_ QOSINFO** de la línea de TSPI hace que TAPI desencadene un evento de QoS. Consulte [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) para obtener información adicional.


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

Identificador de TAPI de la línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Identificador de TAPI de la llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La línea de valor \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Miembro del enumerador [**de \_ eventos QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) que identifica el tipo de evento.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Constante de [tipo de medio](./tapiprotocol--constants.md) que identifica los medios de la llamada asociada a este evento.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_evento QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

