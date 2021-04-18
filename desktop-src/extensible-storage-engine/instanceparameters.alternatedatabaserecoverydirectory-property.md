---
description: 'Más información sobre: InstanceParameters. AlternateDatabaseRecoveryDirectory (propiedad)'
title: Propiedad InstanceParameters. AlternateDatabaseRecoveryDirectory
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705819"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a>Propiedad InstanceParameters. AlternateDatabaseRecoveryDirectory

Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta en la que la recuperación tras bloqueo o una operación de restauración pueden encontrar las bases de datos a las que se hace referencia en el registro de transacciones de la carpeta especificada.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="remarks"></a>Observaciones

Este parámetro se omite en Windows XP.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros de InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
