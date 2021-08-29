---
description: El mensaje TAPI LINE \_ CALLHUBCLOSE se envía cuando se ha cerrado un centro de llamadas.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: LINE_CALLHUBCLOSE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e65c479c54897d3f90406171a2d109434752dc0880893f40b09e5717a28fd21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873605"
---
# <a name="line_callhubclose-message"></a>MENSAJE \_ LINE CALLHUBCLOSE

El mensaje TAPI **LINE \_ CALLHUBCLOSE** se envía cuando se ha cerrado un centro de llamadas.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la llamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Reservado. Establecer en 0.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reservado. Establecer en 0.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este mensaje se origina con TAPI en lugar de con un proveedor de servicios, por lo que no hay ningún mensaje TSPI correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




