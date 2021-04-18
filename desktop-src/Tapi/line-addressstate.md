---
description: El \_ mensaje de línea de ADDRESSSTATE TAPI se envía cuando cambia el estado de una dirección en una línea abierta actualmente por la aplicación. La aplicación puede invocar lineGetAddressStatus para determinar el estado actual de la dirección.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Mensaje de LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679367"
---
# <a name="line_addressstate-message"></a>Mensaje de línea \_ ADDRESSSTATE

El mensaje de **línea de \_ ADDRESSSTATE** TAPI se envía cuando cambia el estado de una dirección en una línea abierta actualmente por la aplicación. La aplicación puede invocar [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) para determinar el estado actual de la dirección.


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

Identificador de dirección de la dirección que cambió de estado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Estado de la dirección que cambió. Puede ser una o varias de las [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje **line \_ ADDRESSSTATE** se envía a cualquier aplicación que haya abierto el dispositivo de línea y que haya habilitado este mensaje. El envío de este mensaje para los distintos elementos de estado se puede controlar y consultar mediante [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) y [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). De forma predeterminada, los informes de estado de direcciones están deshabilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



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

 

 




