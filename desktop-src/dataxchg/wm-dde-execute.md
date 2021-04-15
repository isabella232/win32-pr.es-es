---
title: Mensaje de WM_DDE_EXECUTE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ mensaje de ejecución de WM DDE \_ a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Intercambio de datos de mensajes de WM_DDE_EXECUTE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422376"
---
# <a name="wm_dde_execute-message"></a>Mensaje de ejecución de \_ DDE de WM \_

Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ ejecución de WM DDE** a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos. Se espera que la aplicación de servidor publique un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) en respuesta.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


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

Contiene un objeto de memoria global que hace referencia a una cadena de comandos ANSI o Unicode, en función de los tipos de ventanas que participan en la conversación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La cadena de comandos es una cadena terminada en null que consta de una o varias cadenas de código de operación entre corchetes ( \[ \] ). Cada cadena de código de operación tiene la sintaxis siguiente, donde la lista de *parámetros* es opcional:

*parámetros de código de operación*

El *código de operación* es cualquier token único definido por la aplicación. No puede incluir espacios, comas, paréntesis, corchetes ni comillas.

La lista de *parámetros* puede contener cualquier valor definido por la aplicación o valores. Varios parámetros se separan mediante comas y la lista completa de parámetros se incluye entre paréntesis. Los parámetros no pueden incluir comas ni paréntesis, excepto dentro de una cadena entrecomillada. Si un corchete o un paréntesis van a aparecer en una cadena entrecomillada, no es necesario doblarlo, como era el caso de las reglas anteriores.

Las siguientes son cadenas de comandos válidas:


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



Tenga en cuenta que, en las reglas anteriores, los paréntesis y corchetes tenían que doblarse, como se indica a continuación:


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



Los servidores deben ser capaces de analizar los comandos de cualquier forma.

Las cadenas de ejecución Unicode solo deben usarse cuando los identificadores de la ventana de cliente y de servidor hacen que la función [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) devuelva **true**.

### <a name="posting"></a>Config

La aplicación cliente asigna el objeto de memoria global mediante una llamada a la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .

Al procesar el mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) que el servidor envía en respuesta a un mensaje de **\_ \_ ejecución de WM DDE** , la aplicación cliente debe eliminar el objeto devuelto por el mensaje de **\_ \_ confirmación de DDE de WM** .

### <a name="receiving"></a>Recepción

La aplicación de servidor envía el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa. El servidor debe volver a usar el objeto de memoria global.

A menos que un subprotocolo especifique lo contrario, el servidor no debe exponer el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) hasta que se completen todas las acciones especificadas por la cadena de comando Execute. La única excepción a esta regla es cuando la cadena hace que el servidor finalice la conversación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

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

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_confirmación de DDE de WM \_**](wm-dde-ack.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

