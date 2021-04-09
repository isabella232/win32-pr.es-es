---
description: El evento OnObjectReady de un objeto SWbemSink se desencadena cuando una operación asincrónica devuelve un objeto.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectReady (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155808"
---
# <a name="iswbemsinkeventsonobjectready-event"></a>Evento ISWbemSinkEvents:: OnObjectReady

El evento **OnObjectReady** de un objeto [**SWbemSink**](swbemsink.md) se desencadena cuando una operación asincrónica devuelve un objeto. Utilice este evento para procesar objetos de llamadas asincrónicas como [**SWbemObject. InstancesAsync \_**](swbemobject-instancesasync-.md) o [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md). **OnObjectReady** devuelve un [**SWbemObject**](swbemobject.md) cada vez hasta que se completa la enumeración.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Objeto [**SWbemObject**](swbemobject.md) . Esto es similar a lo que devuelve el equivalente sincrónico de la llamada asincrónica que desencadena este evento. Por ejemplo, una llamada al método [**SWbemServices. GetAsync**](swbemservices-getasync.md) devuelve un **SWbemObject** en el parámetro *objWbemObject* del evento **OnObjectReady** del objeto [**SWbemSink**](swbemsink.md) , que se pasa como parámetro *objWbemObject* de la llamada original. El mismo objeto **SWbemObject** se puede obtener mediante una llamada sincrónica equivalente a [**SWbemServices. Get**](swbemservices-get.md).

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original. Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="error-codes"></a>Códigos de error

Después de la finalización del evento **OnObjectReady** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.

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

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, utilice la comunicación sincrónica o la comunicación sincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

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

 

