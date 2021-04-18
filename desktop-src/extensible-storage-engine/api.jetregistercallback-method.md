---
description: 'Más información sobre: API. JetRegisterCallback (método)'
title: Método API. JetRegisterCallback
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707251"
---
# <a name="apijetregistercallback-method"></a>Método API. JetRegisterCallback

Permite a la aplicación configurar el motor de base de datos para emitir notificaciones a la aplicación para eventos concretos. Estas notificaciones están asociadas a una tabla específica y permanecen en vigor solo hasta que se cierra la instancia que contiene la tabla mediante [JetTerm (JET_INSTANCE)](./api.jetterm-method.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor abierto en la tabla en la que se debe registrar la devolución de llamada.

<!-- end list -->

  - cbtyp  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    Los motivos de devolución de llamada para los que la aplicación desea recibir notificaciones.

<!-- end list -->

  - devolución de llamada  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    La función de devolución de llamada.

<!-- end list -->

  - context  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexto que se proporcionará a la devolución de llamada.

<!-- end list -->

  - callbackId  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Identificador que se puede usar más adelante para cancelar el registro de la función de devolución de llamada determinada mediante [JetUnregisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
