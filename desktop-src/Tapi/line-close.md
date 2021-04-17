---
description: El mensaje de cierre de línea TAPI \_ se envía cuando el dispositivo de línea especificado se ha cerrado forzosamente. Una vez que se ha enviado este mensaje, el identificador del dispositivo de línea o los identificadores de llamada de las llamadas en la línea ya no son válidos.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Mensaje de LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690330"
---
# <a name="line_close-message"></a>Mensaje de cierre de línea \_

El mensaje **de \_ cierre de línea** TAPI se envía cuando el dispositivo de línea especificado se ha cerrado forzosamente. Una vez que se ha enviado este mensaje, el identificador del dispositivo de línea o los identificadores de llamada de las llamadas en la línea ya no son válidos.


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

El mensaje de **\_ cierre de línea** se envía a cualquier aplicación solo después de que el proveedor de servicios TAPI (TSP) haya cerrado de manera forzada una línea abierta. Si la línea se puede volver a abrir inmediatamente después de que un cierre forzado sea específico del dispositivo.

La condición que causa puede ser un cambio significativo del estado, un error de hardware, una pérdida de conexión con un servidor o incluso potencialmente para impedir que una sola aplicación monopolice un dispositivo de línea durante demasiado tiempo. También se puede cerrar un dispositivo de línea una vez que el usuario haya modificado la configuración de esa línea o su controlador. Si el usuario desea que los cambios de configuración surtan efecto inmediatamente (en lugar de después del siguiente reinicio del sistema) y afectan a la vista actual del dispositivo (por ejemplo, un cambio en las capacidades del dispositivo), un proveedor de servicios puede forzar el cierre del dispositivo de línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




