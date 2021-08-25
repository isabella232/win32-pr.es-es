---
description: El mensaje TAPI LINE DEVSPECIFICEX se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una \_ línea, dirección o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: LINE_DEVSPECIFICEX mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b65b322b265b6bbd9717a9fc5b3c0eccf46bb3802fef7684a58d2d69645cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867075"
---
# <a name="line_devspecificex-message"></a>MENSAJE \_ LINE DEVSPECIFICEX

El mensaje **\_ TAPI LINE DEVSPECIFICEX** se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, dirección o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador para un dispositivo de línea o una llamada. Este parámetro es específico del dispositivo.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico del dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico del dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Un proveedor de servicios usa el mensaje **LINE \_ DEVSPECIFICEX** junto con la [**función lineDevSpecific.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




