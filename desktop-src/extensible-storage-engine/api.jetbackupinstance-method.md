---
description: Más información sobre el método Api.JetBackupInstance
title: Método Api.JetBackupInstance
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270076"
---
# <a name="apijetbackupinstance-method"></a>Método Api.JetBackupInstance

Realiza una copia de seguridad de streaming de una instancia, incluidas todas las bases de datos adjuntas, en un directorio. Con varios métodos de copia de seguridad admitidos por el motor, esta es la función más sencilla y encapsulada.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia de la que se copia la copia de seguridad.

<!-- end list -->

  - destination  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Directorio donde se va a almacenar la copia de seguridad. Si la ruta de acceso de copia de seguridad es NULL para usar la función truncará los registros, si es posible.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)  
    
    Opciones de copia de seguridad.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Devolución de llamada de notificación de estado opcional.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
