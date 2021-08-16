---
UID: ''
title: Función de devolución de llamada JournalPlaybackProc
description: Reproduce una serie de mensajes del mouse y el teclado registrados anteriormente.
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
ms.openlocfilehash: bee538bf2c20cc3cadb6f0bdf6f5dd6a2ae12dfe8a21baeb56b8ad62cb23ff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437132"
---
# <a name="journalplaybackproc-function"></a>Función JournalPlaybackProc

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la [función SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
Normalmente, una aplicación usa esta función para reproducir una serie de mensajes del mouse y el teclado registrados anteriormente por el procedimiento de enlace **JournalRecordProc.**
Siempre que se instale un procedimiento de enlace **JournalPlaybackProc,** la entrada normal del mouse y el teclado está deshabilitada.

El **tipo HOOKPROC** define un puntero a esta función de devolución de llamada.
**JournalPlaybackProc es** un marcador de posición para el nombre de función definido por la aplicación o definido por la biblioteca.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="code-in"></a>code [in]

Tipo: **int**

Código que el procedimiento de enlace usa para determinar cómo procesar el mensaje.
Si *el* código es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_GETNEXT** 1 | El procedimiento de enlace debe copiar el mensaje actual del mouse o del teclado en la estructura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) a la que apunta el *parámetro lParam.* |
| **HC_NOREMOVE** 3 | Una aplicación ha llamado **a** la función [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) con wRemoveMsg establecido en PM_NOREMOVE , lo que indica que el mensaje no se quita de la cola de mensajes después del procesamiento **de PeekMessage.** |
| **HC_NOREMOVE** 2 | El procedimiento de enlace debe prepararse para copiar el siguiente mensaje del mouse o del teclado en la **estructura EVENTMSG** a la que *apunta lParam*. Tras recibir el **HC_GETNEXT,** el procedimiento de enlace debe copiar el mensaje en la estructura . |
| **HC_SYSMODALOFF** 5 | Se ha destruyedo un cuadro de diálogo modal del sistema. El procedimiento de enlace debe reanudar la reproducción de los mensajes. |
| **HC_SYSMODALON** 4 | Se muestra un cuadro de diálogo modal del sistema. Hasta que se destruya el cuadro de diálogo, el procedimiento de enlace debe detener la reproducción de mensajes. |

### <a name="wparam"></a>wParam

Tipo: **WPARAM**

Este parámetro no se utiliza.

### <a name="lparam"></a>lParam

Tipo: **LPARAM**

Puntero a una **estructura EVENTMSG** que representa un mensaje que está procesando el procedimiento de enlace.
Este parámetro solo es válido cuando el *parámetro de* código se **HC_GETNEXT**.

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Para que el sistema espere antes de procesar el mensaje, el valor devuelto debe ser la cantidad de tiempo, en tics de reloj, que el sistema debe esperar.

(Este valor se puede calcular calculando la diferencia entre los miembros de tiempo de los mensajes de entrada actuales y anteriores).

Para procesar el mensaje inmediatamente, el valor devuelto debe ser cero. El valor devuelto solo se usa si el código de enlace está **HC_GETNEXT**; De lo contrario, se omite.

## <a name="remarks"></a>Comentarios

Un **procedimiento de enlace JournalPlaybackProc** debe copiar un mensaje de entrada en el parámetro *lParam.*
El mensaje se debe haber registrado previamente mediante un procedimiento de enlace **JournalRecordProc,** que no debe modificar el mensaje.

Para recuperar el mismo mensaje una y otra vez,  se puede llamar varias veces al procedimiento  de enlace con el parámetro de código establecido en **HC_GETNEXT** sin una llamada de intervención con el código establecido en **HC_SKIP**.

Si *el* código **HC_GETNEXT** y el valor devuelto es mayor que cero, el sistema se suspensión durante el número de milisegundos especificado por el valor devuelto. Cuando el sistema continúa, llama de nuevo al procedimiento de enlace con el código *establecido* **en HC_GETNEXT** para recuperar el mismo mensaje.
El valor devuelto de esta nueva llamada a **JournalPlaybackProc** debe ser cero; De lo contrario, el sistema volverá a estar en modo de suspensión durante el número de milisegundos especificado por el valor devuelto, volverá a llamar a **JournalPlaybackProc,** y así sucesivamente.
Parecerá que el sistema no responde.

A diferencia de la mayoría de otros procedimientos de enlace globales, siempre se llama a los procedimientos de enlace **JournalRecordProc** y **JournalPlaybackProc** en el contexto del subproceso que establece el enlace.

Después de que el procedimiento de enlace devuelva el control al sistema, el mensaje se sigue procesando. Si *el* código **HC_SKIP**, el procedimiento de enlace debe prepararse para devolver el siguiente mensaje de evento registrado en su siguiente llamada.

Instale el procedimiento de enlace **JournalPlaybackProc** especificando el tipo [WH_JOURNALPLAYBACK](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la **función SetWindowsHookEx.**

Si el usuario presiona CTRL+ESC O CTRL+ALT+SUPR durante la reproducción del diario, el sistema detiene la reproducción, desenlazna el procedimiento de reproducción del diario y envía un mensaje [WM_CANCELJOURNAL](wm-canceljournal.md) a la aplicación de diario.

Si el procedimiento de enlace devuelve un mensaje en el intervalo **WM_KEYFIRST** para **WM_KEYLAST**, se aplican las condiciones siguientes:

* El **miembro paramL** de la **estructura EVENTMSG** especifica el código de clave virtual de la clave que se presionó.
* El **miembro paramH** de la **estructura EVENTMSG** especifica el código de examen.
* No hay ninguna manera de especificar un recuento de repeticiones.
El evento siempre se toma para representar un evento clave.

## <a name="see-also"></a>Consulte también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Enlaces](hooks.md)
