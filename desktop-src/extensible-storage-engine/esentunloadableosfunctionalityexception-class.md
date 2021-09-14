---
description: 'Más información sobre: Clase EsentUnloadableOSFunctionalityException'
title: Clase EsentUnloadableOSFunctionalityException
TOCTitle: EsentUnloadableOSFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunloadableosfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55107333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81b1151be5020a07f92582e762c6e6597138d9d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126883116"
---
# <a name="esentunloadableosfunctionalityexception-class"></a>Clase EsentUnloadableOSFunctionalityException

Clase base para JET_err. Excepciones UnloadableOSFunctionality.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentFatalException](./esentfatalexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException  

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnloadableOSFunctionalityException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentUnloadableOSFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnloadableOSFunctionalityException : EsentFatalException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentUnloadableOSFunctionalityException](./esentunloadableosfunctionalityexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
