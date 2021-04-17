---
description: El evento OnProgress de SWbemSink se desencadena cuando una llamada asincrónica devuelve el estado de una llamada en curso.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnProgress (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717124"
---
# <a name="iswbemsinkeventsonprogress-event"></a>ISWbemSinkEvents:: OnProgress (evento)

El evento **OnProgress** de [**SWbemSink**](swbemsink.md) se desencadena cuando una llamada asincrónica devuelve el estado de una llamada en curso. Si los eventos, instancias o clases se generan a partir de un proveedor que admite actualizaciones de estado, puede colocar código en este evento para proporcionar a los usuarios comentarios sobre el estado de una operación asincrónica. Debe establecer el parámetro *iFlags* de la llamada asincrónica a **wbemFlagSendStatus** (128/0x80) Si desea recibir actualizaciones de estado, de lo contrario, este evento no se desencadena.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iUpperBound* 
</dt> <dd>

Entero que describe el número total de tareas que se van a completar.

</dd> <dt>

*iCurrent* 
</dt> <dd>

Elemento actual que se está procesando.

</dd> <dt>

*strMessage* 
</dt> <dd>

Mensaje que describe el estado de la tarea actual.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original. Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el evento **OnProgress** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Se produjo un error de red, evitando el funcionamiento normal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El evento **OnProgress** se desencadena cuando una llamada asincrónica devuelve el estado de una llamada en curso. Si los eventos, instancias o clases se generan a partir de un proveedor que admite actualizaciones de estado, puede colocar código en este evento para proporcionar a los usuarios comentarios sobre el estado de una operación asincrónica.

> [!Note]  
> Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | \_ISWBEMSINKEVENTS IID<br/>                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

