---
description: El evento OnObjectPut de un objeto SWbemSink se desencadena cuando se completa una operación PUT asincrónica. Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectPut (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279286"
---
# <a name="iswbemsinkeventsonobjectput-event"></a>Evento ISWbemSinkEvents:: OnObjectPut

El evento **OnObjectPut** de un objeto [**SWbemSink**](swbemsink.md) se desencadena cuando se completa una operación PUT asincrónica. Este evento devuelve la ruta de acceso del objeto de la instancia o la clase guardada.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemObjectPath* 
</dt> <dd>

Objeto [**SWbemObjectPath**](swbemobjectpath.md) que contiene la ruta de acceso del objeto de la instancia o clase que la operación PUT escribe en WMI.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original. Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas con este receptor de objetos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="error-codes"></a>Códigos de error

Después de la finalización del evento **OnObjectPut** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.

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

> [!Note]  
> Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, utilice la comunicación sincrónica o la comunicación sincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

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

 

