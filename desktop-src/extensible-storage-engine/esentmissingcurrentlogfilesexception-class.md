---
description: 'Más información sobre: Clase EsentMissingCurrentLogFilesException'
title: Clase EsentMissingCurrentLogFilesException
TOCTitle: EsentMissingCurrentLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingcurrentlogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcc3e765a7a7e0f9a1ee7af7c5b7224b647bace035c86eeb093b6393715d3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040713"
---
# <a name="esentmissingcurrentlogfilesexception-class"></a>Clase EsentMissingCurrentLogFilesException

Clase base para JET_err. Excepciones missingCurrentLogFiles.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingCurrentLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingCurrentLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingCurrentLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentMissingCurrentLogFilesException](./esentmissingcurrentlogfilesexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
