---
description: 'Más información sobre: Clase EsentFatalException'
title: Clase EsentFatalException
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567069"
---
# <a name="esentfatalexception-class"></a>Clase EsentFatalException

Clase base para excepciones irreales.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentFatalException  
            

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentFatalException](./esentfatalexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentFatalException  
            [Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException](./esentinstanceunavailableexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRollbackErrorException](./esentrollbackerrorexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException](./esentsectorsizenotsupportedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException](./esentunloadableosfunctionalityexception-class.md)