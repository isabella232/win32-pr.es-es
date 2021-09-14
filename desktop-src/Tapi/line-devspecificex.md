---
description: El mensaje TAPI LINE DEVSPECIFICEX se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una \_ línea, dirección o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: LINE_DEVSPECIFICEX mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250148"
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

## <a name="remarks"></a>Observaciones

Un proveedor de servicios usa el mensaje **LINE \_ DEVSPECIFICEX** junto con la [**función lineDevSpecific.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




