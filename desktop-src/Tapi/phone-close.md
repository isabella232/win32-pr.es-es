---
description: El mensaje TAPI PHONE CLOSE se envía cuando se ha cerrado forzadamente un dispositivo de teléfono abierto como parte de \_ la recuperación de recursos. El identificador del dispositivo ya no es válido una vez enviado este mensaje.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: PHONE_CLOSE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071103"
---
# <a name="phone_close-message"></a>Mensaje de PHONE \_ CLOSE

El mensaje TAPI **PHONE \_ CLOSE** se envía cuando se ha cerrado forzadamente un dispositivo de teléfono abierto como parte de la recuperación de recursos. El identificador del dispositivo ya no es válido una vez enviado este mensaje.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Identificador del dispositivo de teléfono abierto que se cerró. El identificador ya no es válido después de que se haya enviado este mensaje.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

La instancia de devolución de llamada de la aplicación que proporcionó al abrir el dispositivo telefónico.

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

El **mensaje \_ PHONE CLOSE** solo se envía a una aplicación después de que se haya cerrado forzadamente un teléfono abierto. Esto se puede hacer para evitar que una sola aplicación pueda tener un dispositivo telefónico durante demasiado tiempo. Si el teléfono se puede volver a abrir inmediatamente después de un cierre forzado es específico del dispositivo.

Un dispositivo de teléfono abierto también se puede cerrar forzadamente después de que el usuario haya modificado la configuración de ese teléfono o su controlador. Si el usuario desea que los cambios de configuración sean efectivos inmediatamente (en lugar de después del siguiente reinicio del sistema) y estos cambios afectan a la vista actual de la aplicación del dispositivo (por ejemplo, un cambio en las funcionalidades del dispositivo), un proveedor de servicios puede cerrar forzadamente el dispositivo telefónico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




