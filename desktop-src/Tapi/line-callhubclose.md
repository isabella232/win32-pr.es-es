---
description: El mensaje TAPI LINE \_ CALLHUBCLOSE se envía cuando se ha cerrado un centro de llamadas.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: LINE_CALLHUBCLOSE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250209"
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

## <a name="remarks"></a>Observaciones

Este mensaje se origina con TAPI en lugar de con un proveedor de servicios, por lo que no hay ningún mensaje TSPI correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




