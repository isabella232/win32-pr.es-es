---
description: 'Más información sobre: Clase EsentOperationException'
title: Clase EsentOperationException
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfa501840c276941d39873dd402d0c0cc949c4ecd2d9bccf59c2d0500534861a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118493967"
---
# <a name="esentoperationexception-class"></a>Clase EsentOperationException

Clase base para las excepciones operation.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        Microsoft.Isam.Esent.Interop.EsentOperationException  
          

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentOperationException](./esentoperationexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        Microsoft.Isam.Esent.Interop.EsentOperationException  
          [Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException](./esentbackupabortbyserverexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException](./esentcheckpointdepthtoodeepexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentClientRequestToStopJetServiceException](./esentclientrequesttostopjetserviceexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentFatalException](./esentfatalexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInitInProgressException](./esentinitinprogressexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInternalErrorException](./esentinternalerrorexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentIOException](./esentioexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException](./esentntsystemcallfailedexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException](./esentossnapshottimeoutexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException](./esentrecordnotdeletedexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentTermInProgressException](./esentterminprogressexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUnicodeLanguageValidationFailureException](./esentunicodelanguagevalidationfailureexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException](./esentunicodetranslationfailexception-class.md)