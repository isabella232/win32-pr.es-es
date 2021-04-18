---
description: 'Más información sobre: API. JetGetAttachInfoInstance (método)'
title: Método API. JetGetAttachInfoInstance
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
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720345"
---
# <a name="apijetgetattachinfoinstance-method"></a>Método API. JetGetAttachInfoInstance

Se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar a una instancia los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad. Solo se tendrán en cuenta las bases de datos que están asociadas actualmente a la instancia mediante [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) . Estos archivos se pueden abrir posteriormente con [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) y leer mediante [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia para la que se va a obtener información.

<!-- end list -->

  - files  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Devuelve una lista de cadenas terminadas en null que describen el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad. La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.

<!-- end list -->

  - maxChars  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número máximo de caracteres que se van a recuperar.

<!-- end list -->

  - actualChars  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Tamaño real de la lista de archivos. Si es mayor que maxChars, la lista se ha truncado.

## <a name="remarks"></a>Observaciones

Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
