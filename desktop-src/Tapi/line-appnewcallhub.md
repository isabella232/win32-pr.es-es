---
description: Se envía el mensaje APPNEWCALLHUB de línea de TAPI \_ para informar a una aplicación cuando se ha creado un nuevo centro de llamadas.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Mensaje de LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680773"
---
# <a name="line_appnewcallhub-message"></a>Mensaje de línea \_ APPNEWCALLHUB

Se envía el mensaje **\_ APPNEWCALLHUB de línea** de TAPI para informar a una aplicación cuando se ha creado un nuevo centro de llamadas.


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

Nivel de seguimiento en el nuevo concentrador, tal y como se define en una de las [**\_ constantes de LINECALLHUBTRACKING**](linecallhubtracking--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje se origina con TAPI en lugar de con un proveedor de servicios, por lo que no hay ningún mensaje TSPI correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




