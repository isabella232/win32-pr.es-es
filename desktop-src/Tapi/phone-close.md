---
description: El mensaje de cierre del teléfono TAPI \_ se envía cuando un dispositivo telefónico abierto se ha cerrado forzosamente como parte de la recuperación de recursos. El identificador de dispositivo ya no es válido una vez que se ha enviado el mensaje.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Mensaje de PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680426"
---
# <a name="phone_close-message"></a>Mensaje de cierre del teléfono \_

El mensaje **de \_ cierre del teléfono** TAPI se envía cuando un dispositivo telefónico abierto se ha cerrado forzosamente como parte de la recuperación de recursos. El identificador de dispositivo ya no es válido una vez que se ha enviado el mensaje.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Identificador del dispositivo de teléfono abierto que se cerró. El identificador ya no es válido después de enviar este mensaje.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada de la aplicación que se proporciona al abrir el dispositivo telefónico.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje de **\_ cierre de teléfono** solo se envía a una aplicación después de que se haya cerrado un teléfono abierto. Esto se puede hacer para evitar que una sola aplicación monopolice un dispositivo telefónico durante demasiado tiempo. Si el teléfono se puede volver a abrir inmediatamente después de que un cierre forzado sea específico del dispositivo.

También se puede cerrar un dispositivo telefónico abierto después de que el usuario haya modificado la configuración de ese teléfono o su controlador. Si el usuario desea que los cambios de configuración se apliquen de inmediato (en lugar de después del siguiente reinicio del sistema) y estos cambios afectan a la vista actual del dispositivo (por ejemplo, un cambio en las capacidades del dispositivo), un proveedor de servicios puede forzar el cierre del dispositivo telefónico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




