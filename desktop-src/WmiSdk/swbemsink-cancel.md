---
description: El método CANCEL del objeto SWbemSink cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'ISWbemSink:: CANCEL (método) (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279287"
---
# <a name="iswbemsinkcancel-method"></a>ISWbemSink:: CANCEL (método)

El método **Cancel** del objeto [**SWbemSink**](swbemsink.md) cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Cancel** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.

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

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

El nombre de usuario y la contraseña actuales o especificados no son válidos o están autorizados para establecer la conexión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se puede cancelar solo una llamada asincrónica. Si hay varias llamadas asincrónicas pendientes que utilizan este receptor de objetos, este método cancela todas las llamadas asincrónicas que utilizan este receptor de objetos. Las llamadas asincrónicas que están asociadas a otros receptores de objeto continúan sin efecto.

No se puede asignar este receptor a **Nothing** para cancelar una operación asincrónica. Debe llamar al método **Cancel** para que WMI interrumpa la operación y libere los recursos asociados. Esto es muy importante con operaciones asincrónicas largas, como consultas u operaciones que nunca se completan, como [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

En el ejemplo siguiente se muestra cómo cancelar una llamada asincrónica.


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | \_ISWBEMSINK IID<br/>                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

