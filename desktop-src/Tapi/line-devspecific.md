---
description: El mensaje TAPI LINE DEVSPECIFIC se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una \_ línea, dirección o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: LINE_DEVSPECIFIC mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca1ba410ac3127ff917965e8eda7c579be68dab5150c6dcae63a1930a98d265
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975675"
---
# <a name="line_devspecific-message"></a>MENSAJE \_ LINE DEVSPECIFIC

El mensaje **\_ TAPI LINE DEVSPECIFIC** se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, dirección o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador para un dispositivo de línea o una llamada. Esto es específico del dispositivo.

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

Un proveedor de servicios usa el mensaje **LINE \_ DEVSPECIFIC** junto con la [**función lineDevSpecific.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




