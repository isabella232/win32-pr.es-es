---
description: El método Cancel del objeto SWbemSink cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: Método ISWbemSink::Cancel (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465972"
---
# <a name="iswbemsinkcancel-method"></a>MÉTODO ISWbemSink::Cancel

El **método Cancel** del objeto [**SWbemSink**](swbemsink.md) cancela todas las operaciones asincrónicas pendientes asociadas a este receptor de objetos.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Cancel,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error siguientes.

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

</dd> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El nombre de usuario y la contraseña actuales o especificados no son válidos ni están autorizados para realizar la conexión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se puede cancelar solo una llamada asincrónica. Si hay varias llamadas asincrónicas pendientes que usan este receptor de objetos, este método cancela todas las llamadas asincrónicas mediante este receptor de objetos. Las llamadas asincrónicas asociadas a otros receptores de objetos no se ven afectadas.

No se puede asignar este receptor a **Nothing para** cancelar una operación asincrónica. Debe llamar al método **Cancel para** que WMI deje de realizar la operación y liberar los recursos asociados. Esto es muy importante con operaciones asincrónicas largas, como consultas u operaciones que nunca se completan, como [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincronosa o sincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

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
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSink<br/>                                                              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

