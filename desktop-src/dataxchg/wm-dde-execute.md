---
title: WM_DDE_EXECUTE mensaje (Dde.h)
description: Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje WM DDE EXECUTE a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de \_ \_ comandos.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160487"
---
# <a name="wm_dde_execute-message"></a>Mensaje \_ EXECUTE de WM DDE \_

Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje **\_ WM DDE \_ EXECUTE** a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos. Se espera que la aplicación de servidor publique un [**mensaje \_ wm DDE \_ ACK**](wm-dde-ack.md) en respuesta.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un objeto de memoria global que hace referencia a una cadena de comandos ANSI o Unicode, en función de los tipos de ventanas implicadas en la conversación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La cadena de comando es una cadena terminada en NULL que consta de una o varias cadenas de código de operación entre corchetes únicos ( \[ \] ). Cada cadena de código de operación tiene la siguiente sintaxis, donde la *lista de parámetros* es opcional:

*parámetros de código de operación*

El *código de operación* es cualquier token único definido por la aplicación. No puede incluir espacios, comas, paréntesis, corchetes ni comillas.

La *lista* de parámetros puede contener cualquier valor o valor definido por la aplicación. Varios parámetros están separados por comas y toda la lista de parámetros se incluye entre paréntesis. Los parámetros no pueden incluir comas ni paréntesis, excepto dentro de una cadena entre comillas. Si un carácter de corchete o paréntesis va a aparecer en una cadena entre comillas, no es necesario duplicarlo, como en el caso de las reglas antiguas.

Las siguientes son cadenas de comandos válidas:


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



Tenga en cuenta que, en las reglas antiguas, los paréntesis y corchetes tenían que duplicarse, como se muestra a continuación:


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



Los servidores deben poder analizar comandos de cualquier forma.

Las cadenas de ejecución Unicode solo se deben usar cuando los identificadores de ventana de cliente y servidor hacen que [**la función IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) devuelva **TRUE.**

### <a name="posting"></a>Publicar

La aplicación cliente asigna el objeto de memoria global mediante una llamada a la [**función GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc)

Al procesar el [**mensaje \_ DDE \_ ACK**](wm-dde-ack.md) de WM que el servidor publica en respuesta a un mensaje **WM \_ DDE \_ EXECUTE,** la aplicación cliente debe eliminar el objeto devuelto por el **mensaje \_ DDE \_ ACK** de WM.

### <a name="receiving"></a>Recepción

La aplicación de servidor publica el [**mensaje \_ WM DDE \_ ACK**](wm-dde-ack.md) para responder de forma positiva o negativa. El servidor debe reutilizar el objeto de memoria global.

A menos que un subprototo especifique lo contrario, el servidor no debe publicar el mensaje [**\_ WM DDE \_ ACK**](wm-dde-ack.md) hasta que se completen todas las acciones especificadas por la cadena de comando execute. La única excepción a esta regla es cuando la cadena hace que el servidor finalice la conversación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Dde.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**DesempaquetarDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

