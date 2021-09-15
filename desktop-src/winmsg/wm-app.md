---
description: Se usa para definir mensajes privados, normalmente con el formato WM \_ APP+x, donde x es un valor entero.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466508"
---
# <a name="wm_app"></a>APLICACIÓN \_ WM

Se usa para definir mensajes privados, normalmente con el formato **WM \_ APP** + *x*, donde *x* es un valor entero.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Observaciones

La **constante \_ WM APP** se usa para distinguir entre los valores de mensaje que están reservados para su uso por el sistema y los valores que puede usar una aplicación para enviar mensajes dentro de una clase de ventana privada. Estos son los intervalos de números de mensaje disponibles.



| Intervalo                                                 | Significado                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 a [**WM \_ USER**](wm-user.md) –1<br/>   | Mensajes reservados para su uso por el sistema.<br/>            |
| [**WM \_ USUARIO**](wm-user.md) a 0x7FFF<br/> | Mensajes enteros para su uso por clases de ventana privadas.<br/> |
| **WM \_ Aplicación** a 0xBFFF<br/>                 | Mensajes disponibles para su uso por las aplicaciones.<br/>         |
| 0xC000 a 0xFFFF<br/>                      | Mensajes de cadena para que los usen las aplicaciones.<br/>            |
| Mayor que 0xFFFF<br/>                        | Reservado por el sistema.<br/>                             |



 

El sistema define los números de mensaje del primer intervalo (de 0 a [**WM \_ USER**](wm-user.md) –1). El sistema reserva los valores de este intervalo que no se definen explícitamente.

Los números de mensaje del segundo intervalo [**(WM \_ USER**](wm-user.md) a 0x7FFF) los puede definir y usar una aplicación para enviar mensajes dentro de una clase de ventana privada. Estos valores no se pueden usar para definir mensajes significativos en toda una aplicación porque algunas clases de ventana predefinidas ya definen valores en este intervalo. Por ejemplo, las clases de control predefinidas **como BUTTON,** **EDIT,** **LISTBOX** y **COMBOBOX** pueden usar estos valores. Los mensajes de este intervalo no deben enviarse a otras aplicaciones a menos que las aplicaciones se hayan diseñado para intercambiar mensajes y para adjuntar el mismo significado a los números de mensaje.

Los números de mensaje del tercer intervalo (0x8000 a 0xBFFF) están disponibles para que las aplicaciones las usen como mensajes privados. Los mensajes de este intervalo no entren en conflicto con los mensajes del sistema.

Los números de mensaje del cuarto intervalo (0xC000 a 0xFFFF) se definen en tiempo de ejecución cuando una aplicación llama a la función [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar un número de mensaje para una cadena. Todas las aplicaciones que registran la misma cadena pueden usar el número de mensaje asociado para intercambiar mensajes. Sin embargo, el número de mensaje real no es una constante y no se puede suponer que sea el mismo entre sesiones diferentes.

El sistema reserva los números de mensaje en el quinto intervalo (0xFFFF) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**WM \_ USER**](wm-user.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Mensajes y colas de mensajes](messages-and-message-queues.md)
</dt> </dl>

 

 
