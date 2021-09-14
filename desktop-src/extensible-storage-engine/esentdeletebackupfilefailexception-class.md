---
description: 'Más información sobre: Clase EsentDeleteBackupFileFailException'
title: Clase EsentDeleteBackupFileFailException
TOCTitle: EsentDeleteBackupFileFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdeletebackupfilefailexception(v=EXCHG.10)
ms:contentKeyID: 55101602
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 193acd73388640123ef0471d8391cb05e44cd4aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361254"
---
# <a name="esentdeletebackupfilefailexception-class"></a>Clase EsentDeleteBackupFileFailException

Clase base para JET_err. DeleteBackupFileFail exceptions.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentIOException](./esentioexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDeleteBackupFileFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentDeleteBackupFileFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDeleteBackupFileFailException : EsentIOException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentDeleteBackupFileFailException](./esentdeletebackupfilefailexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
