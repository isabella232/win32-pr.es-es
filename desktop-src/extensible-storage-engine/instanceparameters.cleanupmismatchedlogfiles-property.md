---
description: 'Más información sobre: InstanceParameters. CleanupMismatchedLogFiles (propiedad)'
title: Propiedad InstanceParameters. CleanupMismatchedLogFiles
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155404"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a>Propiedad InstanceParameters. CleanupMismatchedLogFiles

Obtiene o establece un valor que indica si se produce un error en JetInit cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en un disco con un tamaño diferente del configurado. Normalmente, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) recuperará correctamente las bases de datos, pero producirá un error con [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) para indicar que el tamaño del archivo de registro está mal configurado. Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará silenciosamente todos los archivos de registro antiguos, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño del archivo de registro configurado. Este parámetro es útil cuando la aplicación desea cambiar de forma transparente el tamaño del archivo de registro de transacciones todavía funciona de forma transparente en los escenarios de actualización y restauración.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
