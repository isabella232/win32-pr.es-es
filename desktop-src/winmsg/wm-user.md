---
description: Se usa para definir mensajes privados para su uso por parte de clases de ventana privadas, normalmente con el formato WM \_ User + x, donde x es un valor entero.
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: WM_USER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1efd6f2e79180b7dc627281829539d20f5fa74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082087"
---
# <a name="wm_user"></a>usuario de WM \_

Se usa para definir mensajes privados para su uso por parte de clases de ventana privadas, normalmente con el formato **WM \_ User** + *x*, donde *x* es un valor entero.

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a>Observaciones

A continuación se muestran los intervalos de números de mensaje.



| Intervalo                                                        | Significado                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| de 0 a **WM \_ usuario** – 1<br/>                         | Mensajes reservados para su uso por el sistema.<br/>            |
| **WM \_ USUARIO** a través de 0x7FFF<br/>                       | Mensajes enteros para su uso por las clases de ventana privadas.<br/> |
| [**WM \_ APLICACIÓN**](wm-app.md) (0x8000) a través de 0xBFFF<br/> | Mensajes disponibles para que las usen las aplicaciones.<br/>         |
| 0xC000 a 0xFFFF<br/>                             | Mensajes de cadena para su uso por parte de las aplicaciones.<br/>            |
| Mayor que 0xFFFF<br/>                               | Reservado por el sistema.<br/>                             |



 

El sistema define los números de mensaje en el primer intervalo (del 0 al **\_ usuario de WM** -1). El sistema reserva los valores de este intervalo que no se definen explícitamente.

Los números de mensajes del segundo intervalo **( \_ usuario de WM** a través de 0x7FFF) se pueden definir y usar en una aplicación para enviar mensajes dentro de una clase de ventana privada. Estos valores no se pueden usar para definir mensajes que sean significativos en una aplicación porque algunas clases de ventana predefinidas ya definen valores en este intervalo. Por ejemplo, las clases de control predefinidas como **Button**, **Edit**, **ListBox** y **ComboBox** pueden utilizar estos valores. Los mensajes de este intervalo no se deben enviar a otras aplicaciones a menos que las aplicaciones se hayan diseñado para intercambiar mensajes y adjuntar el mismo significado a los números de mensaje.

Los números de mensaje en el tercer intervalo (de 0x8000 a 0xBFFF) están disponibles para que las aplicaciones lo usen como mensajes privados. Los mensajes de este intervalo no entran en conflicto con los mensajes del sistema.

Los números de mensaje del cuarto intervalo (de 0xC000 a 0xFFFF) se definen en tiempo de ejecución cuando una aplicación llama a la función [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar un número de mensaje para una cadena. Todas las aplicaciones que registran la misma cadena pueden usar el número de mensaje asociado para intercambiar mensajes. Sin embargo, el número de mensaje real no es una constante y no se puede suponer que sea el mismo entre distintas sesiones.

El sistema reserva los números de mensaje del quinto intervalo (mayor que 0xFFFF).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**aplicación de WM \_**](wm-app.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Mensajes y colas de mensajes](messages-and-message-queues.md)
</dt> </dl>

 

 
