---
description: Más información sobre el método Api.JetRestoreInstance
title: Método Api.JetRestoreInstance
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070323"
---
# <a name="apijetrestoreinstance-method"></a>Método Api.JetRestoreInstance

Restaura y recupera una copia de seguridad de streaming de una instancia, incluidas todas las bases de datos adjuntas. Está diseñado para funcionar con una copia de seguridad creada con la función [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS).](./api.jetbackupinstance-method.md) Se trata de la función de restauración más sencilla y encapsulada.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    La instancia de que se utilizará. No se debe inicializar la instancia de . La restauración de los archivos inicializará la instancia.

<!-- end list -->

  - source  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Ubicación de la copia de seguridad. La copia de seguridad se debe haber creado [con JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS).](./api.jetbackupinstance-method.md)

<!-- end list -->

  - destination  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre de la carpeta donde se copiarán y recuperarán los archivos de base de datos del conjunto de copia de seguridad. Si se establece en NULL, los archivos de base de datos se copiarán y recuperarán en su ubicación original.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Devolución de llamada de notificación de estado opcional.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
