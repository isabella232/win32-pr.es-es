---
description: 'Más información sobre: clase EsentDiskReadVerificationFailureException'
title: Clase EsentDiskReadVerificationFailureException
TOCTitle: EsentDiskReadVerificationFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskreadverificationfailureexception(v=EXCHG.10)
ms:contentKeyID: 55101620
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f429efb66f5993f438e132ed564f110e88d234a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279068"
---
# <a name="esentdiskreadverificationfailureexception-class"></a>Clase EsentDiskReadVerificationFailureException

Clase base para JET_err. Excepciones DiskReadVerificationFailure.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDiskReadVerificationFailureException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskReadVerificationFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDiskReadVerificationFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskReadVerificationFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentDiskReadVerificationFailureException](./esentdiskreadverificationfailureexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
