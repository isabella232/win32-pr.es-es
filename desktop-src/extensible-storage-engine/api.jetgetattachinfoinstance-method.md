---
description: Más información sobre el método Api.JetGetAttachInfoInstance
title: Método Api.JetGetAttachInfoInstance
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29796919302b19b708878feb31e1fd53151700694a67bd1f6943bfa9d82d419c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272461"
---
# <a name="apijetgetattachinfoinstance-method"></a>Método Api.JetGetAttachInfoInstance

Se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar en una instancia los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad. Solo se tendrán en cuenta las bases de datos que están asociadas actualmente a la instancia mediante [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit).](./api.jetattachdatabase-method.md) Estos archivos se pueden abrir posteriormente mediante [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) y leerse mediante [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32).](./api.jetreadfileinstance-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia de para la que se obtiene la información.

<!-- end list -->

  - files  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Devuelve una lista de cadenas terminadas en NULL que describen el conjunto de archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad. La lista de cadenas devueltas en este búfer tiene el mismo formato que una cadena múltiple usada por el Registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador null final.

<!-- end list -->

  - maxChars  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Número máximo de caracteres que se recuperarán.

<!-- end list -->

  - actualChars  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Tamaño real de la lista de archivos. Si es mayor que maxChars, la lista se ha truncado.

## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que esta API no devuelve un error o una advertencia si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
