---
UID: ''
title: Función de devolución de llamada JournalPlaybackProc
description: Reproduce una serie de mensajes de teclado y del mouse grabados anteriormente.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "104420504"
---
# <a name="journalplaybackproc-function"></a>JournalPlaybackProc función)

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Normalmente, una aplicación usa esta función para reproducir una serie de mensajes del mouse y del teclado grabados previamente por el procedimiento de enlace **JournalRecordProc** .
Siempre que se instale un procedimiento de enlace **JournalPlaybackProc** , se deshabilitará la entrada normal del mouse y del teclado.

El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.
**JournalPlaybackProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.
Si el *código* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_GETNEXT** 1 | El procedimiento de enlace debe copiar el mouse actual o el mensaje de teclado en la estructura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) señalada por el parámetro *lParam* . |
| **HC_NOREMOVE** 3 | Una aplicación ha llamado a la función [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) con wRemoveMsg establecido en **PM_NOREMOVE**, lo que indica que el mensaje no se quita de la cola de mensajes después del procesamiento de **PeekMessage** . |
| **HC_NOREMOVE** 2 | El procedimiento de enlace debe prepararse para copiar el siguiente mensaje del mouse o del teclado en la estructura **EVENTMSG** a la que apunta *lParam*. Al recibir el código **HC_GETNEXT** , el procedimiento de enlace debe copiar el mensaje en la estructura. |
| **HC_SYSMODALOFF** 5 | Se ha destruido un cuadro de diálogo modal del sistema. El procedimiento de enlace debe reanudar la reproducción de los mensajes. |
| **HC_SYSMODALON** 4 | Se está mostrando un cuadro de diálogo modal del sistema. Hasta que se destruya el cuadro de diálogo, el procedimiento de enlace debe detener la reproducción de mensajes. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parámetro no se utiliza.

### <a name="lparam"></a>lParam

Tipo: **lParam**

Puntero a una estructura **EVENTMSG** que representa un mensaje procesado por el procedimiento de enlace.
Este parámetro solo es válido cuando el parámetro de *código* es **HC_GETNEXT**.

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Para que el sistema espere antes de procesar el mensaje, el valor devuelto debe ser la cantidad de tiempo, en ciclos de reloj, que el sistema debe esperar.

(Este valor se puede calcular calculando la diferencia entre los miembros de hora de los mensajes de entrada actuales y anteriores).

Para procesar el mensaje inmediatamente, el valor devuelto debe ser cero. El valor devuelto se usa solo si el código de enlace es **HC_GETNEXT**; de lo contrario, se omite.

## <a name="remarks"></a>Observaciones

Un procedimiento de enlace **JournalPlaybackProc** debe copiar un mensaje de entrada en el parámetro *lParam* .
El mensaje se debe haber registrado previamente mediante un procedimiento de enlace **JournalRecordProc** , que no debe modificar el mensaje.

Para recuperar el mismo mensaje una y otra vez, se puede llamar varias veces al procedimiento de enlace con el parámetro de *código* establecido en **HC_GETNEXT** sin una llamada intermedia con el *código* establecido en **HC_SKIP**.

Si el *código* es **HC_GETNEXT** y el valor devuelto es mayor que cero, el sistema se suspende durante el número de milisegundos especificado por el valor devuelto. Cuando el sistema continúa, llama de nuevo al procedimiento de enlace con el *código* establecido en **HC_GETNEXT** para recuperar el mismo mensaje.
El valor devuelto de esta nueva llamada a **JournalPlaybackProc** debe ser cero; de lo contrario, el sistema volverá a entrar en suspensión durante el número de milisegundos especificado por el valor devuelto, llamará de nuevo a **JournalPlaybackProc** , etc.
Parecerá que el sistema no responde.

A diferencia de la mayoría de los demás procedimientos de enlace global, siempre se llama a los procedimientos de enlace **JournalRecordProc** y **JournalPlaybackProc** en el contexto del subproceso que establece el enlace.

Una vez que el procedimiento de enlace devuelve el control al sistema, el mensaje continúa procesándose. Si el *código* es **HC_SKIP**, el procedimiento de enlace debe prepararse para devolver el siguiente mensaje de evento registrado en la siguiente llamada.

Instale el procedimiento de enlace **JournalPlaybackProc** especificando el tipo de [WH_JOURNALPLAYBACK](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .

Si el usuario presiona CTRL + ESC o CTRL + ALT + Supr durante la reproducción del diario, el sistema detiene la reproducción, desenlaza el procedimiento de reproducción del diario y envía un mensaje de [WM_CANCELJOURNAL](wm-canceljournal.md) a la aplicación de registro en diario.

Si el procedimiento de enlace devuelve un mensaje en el intervalo **WM_KEYFIRST** a **WM_KEYLAST**, se aplican las condiciones siguientes:

* El miembro **paraml** de la estructura **EVENTMSG** especifica el código de tecla virtual de la tecla que se presionó.
* El miembro **paramH** de la estructura **EVENTMSG** especifica el código de recorrido.
* No hay ninguna manera de especificar un número de repeticiones.
Siempre se toma el evento para representar un evento de clave.

## <a name="see-also"></a>Vea también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Enlaces](hooks.md)
