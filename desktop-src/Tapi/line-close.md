---
description: El mensaje TAPI LINE CLOSE se envía cuando se ha cerrado forzadamente el dispositivo \_ de línea especificado. El identificador de dispositivo de línea o cualquier identificador de llamada para las llamadas en la línea ya no son válidos una vez enviado este mensaje.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: LINE_CLOSE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250202"
---
# <a name="line_close-message"></a>Mensaje \_ LINE CLOSE

El mensaje TAPI **LINE \_ CLOSE** se envía cuando se ha cerrado forzadamente el dispositivo de línea especificado. El identificador de dispositivo de línea o cualquier identificador de llamada para las llamadas en la línea ya no son válidos una vez enviado este mensaje.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del dispositivo de línea que se cerró. Este identificador ya no es válido.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

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

El **mensaje \_ LINE CLOSE** se envía a cualquier aplicación solo después de que el proveedor de servicios TAPI (TSP) haya cerrado forzadamente una línea abierta. Si la línea se puede volver a abrir inmediatamente después de un cierre forzado es específica del dispositivo.

La condición que causa puede ser un cambio significativo de estado, un error de hardware, una pérdida de conexión a un servidor o incluso, potencialmente, impedir que una sola aplicación acote un dispositivo de línea durante demasiado tiempo. Un dispositivo de línea también se puede cerrar forzadamente después de que el usuario haya modificado la configuración de esa línea o su controlador. Si el usuario desea que los cambios de configuración sean efectivos inmediatamente (en lugar de después del siguiente reinicio del sistema) y afectan a la vista actual de la aplicación del dispositivo (por ejemplo, un cambio en las funcionalidades del dispositivo), un proveedor de servicios puede cerrar forzadamente el dispositivo de línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




