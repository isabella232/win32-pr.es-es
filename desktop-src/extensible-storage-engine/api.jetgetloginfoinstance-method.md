---
description: Más información sobre el método Api.JetGetLogInfoInstance
title: Método Api.JetGetLogInfoInstance
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 044e3a214a520ecb331956108eb83449b689decbd995f4b5b9330fdef6729a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670375"
---
# <a name="apijetgetloginfoinstance-method"></a>Método Api.JetGetLogInfoInstance

Se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar una instancia de los nombres de los archivos de revisión de base de datos y los archivos de registro que deben formar parte del conjunto de archivos de copia de seguridad. Estos archivos se pueden abrir posteriormente mediante [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) y leer con [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32).](./api.jetreadfileinstance-method.md)

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
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
    
    Devuelve una lista de cadenas terminadas en NULL que describen el conjunto de archivos de revisión de base de datos y los archivos de registro que deben formar parte del conjunto de archivos de copia de seguridad. La lista de cadenas devueltas en este búfer tiene el mismo formato que una cadena múltiple utilizada por el Registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador null final.

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

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
