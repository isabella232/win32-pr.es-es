---
description: 'Más información sobre: clase EsentMissingCurrentLogFilesException'
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
ms.openlocfilehash: c00bec8ba2dee02bf0240bda78f29b3b8f4eafa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677601"
---
# <a name="esentmissingcurrentlogfilesexception-class"></a>Clase EsentMissingCurrentLogFilesException

Clase base para JET_err. Excepciones MissingCurrentLogFiles.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentMissingCurrentLogFilesException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

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

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
