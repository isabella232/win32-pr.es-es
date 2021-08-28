---
description: El mensaje TAPI LINE ADDRESSSTATE se envía cuando cambia el estado de una dirección en una línea abierta \_ actualmente por la aplicación. La aplicación puede invocar lineGetAddressStatus para determinar el estado actual de la dirección.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: LINE_ADDRESSSTATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfc158bd41b635142252546fbc289ed868851a3ac79d80bddba2df6118715bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959885"
---
# <a name="line_addressstate-message"></a>Mensaje \_ LINE ADDRESSSTATE

El mensaje TAPI **LINE \_ ADDRESSSTATE** se envía cuando cambia el estado de una dirección en una línea abierta actualmente por la aplicación. La aplicación puede invocar [**lineGetAddressStatus para**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) determinar el estado actual de la dirección.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del dispositivo de línea.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de dirección de la dirección que cambió el estado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Estado de dirección que ha cambiado. Puede ser una o varias de las [**constantes LINEADDRESSSTATE \_**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE ADDRESSSTATE** se envía a cualquier aplicación que haya abierto el dispositivo de línea y que haya habilitado este mensaje. El envío de este mensaje para los distintos elementos de estado se puede controlar y consultar mediante [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) y [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). De forma predeterminada, los informes de estado de dirección están deshabilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




