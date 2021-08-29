---
description: El evento OnCompleted de un objeto SWbemSink se desencadena cuando se completa una llamada asincrónica. Este evento indica a la aplicación cliente, el resultado de una operación asincrónica, y proporciona información de error cuando se produce un error en la llamada asincrónica.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: Evento ISWbemSinkEvents::OnCompleted (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 48e326c06c1cb9a17176e5fb71016c1cf23dde628eff9aed1f8e3b49d597786a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050063"
---
# <a name="iswbemsinkeventsoncompleted-event"></a>Evento ISWbemSinkEvents::OnCompleted

El **evento OnCompleted** de un [**objeto SWbemSink**](swbemsink.md) se desencadena cuando se completa una llamada asincrónica. Este evento indica a la aplicación cliente, el resultado de una operación asincrónica, y proporciona información de error cuando se produce un error en la llamada asincrónica.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iHResult* 
</dt> <dd>

HRESULT del método asincrónico completado. HRESULT es el mismo que el valor que se devuelve desde una [API COM equivalente para la llamada al método WMI.](com-api-for-wmi.md) Compruebe este valor para determinar si la llamada asincrónica es correcta o no. Si la llamada asincrónica se realiza correctamente, este parámetro contiene WBEM \_ S \_ NO ERROR \_ (0). Si se produce un error en la llamada asincrónica, este parámetro contiene un código de error.

</dd> <dt>

*objWbemErrorObject* 
</dt> <dd>

Contiene un [**objeto SWbemLastError**](swbemlasterror.md) cuando se produce un error en el método asincrónico.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Se trata de [**un objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que se pasa a la llamada asincrónica original. Use este parámetro para identificar el origen de la llamada asincrónica que desencadena este evento cuando se realizan varias llamadas asincrónicas mediante este receptor de objetos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el **evento OnCompleted,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> <dt>

**wbemErrTransportFailure:** 2147749909 (0x80041015)
</dt> <dd>

Error de red, lo que impide el funcionamiento normal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincronosa o sincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



 

