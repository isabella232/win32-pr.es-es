---
UID: ''
title: Función de devolución de llamada JournalRecordProc
description: La función registra los mensajes que el sistema quita de la cola de mensajes del sistema.
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
ms.openlocfilehash: cc5e1bdbd99b234b347d0b9c10caa7125aead9b68138472e125c8e2a11180609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437122"
---
# <a name="journalrecordproc-function"></a>Función JournalRecordProc

## <a name="description"></a>Descripción

Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la [función SetWindowsHookEx.](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)
La función registra los mensajes que el sistema quita de la cola de mensajes del sistema.
Más adelante, una aplicación puede usar un procedimiento de enlace [JournalPlaybackProc](journalplaybackproc.md) para reproducir los mensajes.

El **tipo HOOKPROC** define un puntero a esta función de devolución de llamada.
**JournalRecordProc es** un marcador de posición para el nombre de la función definida por la aplicación o definida por la biblioteca.

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parámetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Especifica cómo procesar el mensaje.
Si *el* código es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin procesarlo más y debe devolver el valor devuelto por **CallNextHookEx**.
Este parámetro puede ser uno de los valores siguientes.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | El *parámetro lParam* es un puntero a una [estructura EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) que contiene información sobre un mensaje quitado de la cola del sistema. El procedimiento de enlace debe registrar el contenido de la estructura cópielos en un búfer o archivo. |
| **HC_SYSMODALOFF** 5 | Se ha destruido un cuadro de diálogo modal del sistema. El procedimiento de enlace debe reanudar la grabación. |
| **HC_SYSMODALON** 4 | Se muestra un cuadro de diálogo modal del sistema. Hasta que se destruya el cuadro de diálogo, el procedimiento de enlace debe detener la grabación. |

### <a name="wparam"></a>wParam

Tipo: **WPARAM**

Este parámetro no se utiliza.

### <a name="lparam-in"></a>lParam [in]

Tipo: **LPARAM**

Puntero a una **estructura EVENTMSG** que contiene el mensaje que se va a registrar.

## <a name="returns"></a>Devoluciones

Tipo: **LRESULT**

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Un **procedimiento de enlace JournalRecordProc** debe copiar pero no modificar los mensajes.
Una vez que el procedimiento de enlace devuelve el control al sistema, el mensaje se sigue procesando.

Instale el procedimiento de enlace **JournalRecordProc** especificando el tipo [WH_JOURNALRECORD](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx.**

Un **procedimiento de enlace JournalRecordProc** no necesita estar en una biblioteca de vínculos dinámicos.
Un **procedimiento de enlace JournalRecordProc** puede estar en directo en la propia aplicación.

A diferencia de la mayoría de los demás procedimientos de enlace globales, siempre se llama a los procedimientos de enlace **JournalRecordProc** y [JournalPlaybackProc](journalplaybackproc.md) en el contexto del subproceso que establece el enlace.

Una aplicación que haya instalado un procedimiento de enlace **JournalRecordProc** debe observar el código de clave virtual de [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (que se implementa como combinación de teclas CTRL+BREAK en la mayoría de los teclados).
La aplicación debe interpretar este código de clave virtual como una señal de que el usuario desea detener la grabación del diario.
La aplicación debe responder finalizando la secuencia de grabación y quitando el procedimiento de enlace **JournalRecordProc.**
La eliminación es importante.
Impide que una aplicación de registro en diario bloquee el sistema al bloquearse dentro de un procedimiento de enlace.

Este rol como señal para detener la grabación de la sesión significa que no se puede grabar una combinación de teclas CTRL+BREAK.
Puesto que la combinación de teclas CTRL+C no tiene tal rol como señal de diario, se puede registrar.
Hay otras dos combinaciones de teclas que no se pueden grabar: CTRL+ESC y CTRL+ALT+SUPR.
Estas dos combinaciones de claves hacen que el sistema detenga todas las actividades de [](wm-canceljournal.md) registro en diario (grabación o reproducción), quite todos los enlaces de registro y publique un mensaje WM_CANCELJOURNAL en la aplicación de registro en diario.

## <a name="see-also"></a>Consulte también

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Enlaces](hooks.md)
