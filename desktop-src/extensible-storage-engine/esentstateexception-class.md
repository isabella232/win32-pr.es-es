---
description: 'Más información sobre: clase EsentStateException'
title: Clase EsentStateException
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279743"
---
# <a name="esentstateexception-class"></a>Clase EsentStateException

Clase base para las excepciones de estado.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentStateException  
            

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentStateException](./esentstateexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentStateException  
            [Microsoft. ISAM. esent. Interop. EsentBackupInProgressException](./esentbackupinprogressexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBackupNotAllowedYetException](./esentbackupnotallowedyetexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadItagSequenceException](./esentbaditagsequenceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBufferTooSmallException](./esentbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCallbackFailedException](./esentcallbackfailedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseAlreadyUpgradedException](./esentdatabasealreadyupgradedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseFailedIncrementalReseedException](./esentdatabasefailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseIncompleteUpgradeException](./esentdatabaseincompleteupgradeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseLeakInSpaceException](./esentdatabaseleakinspaceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDirtyShutdownException](./esentdirtyshutdownexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileNotFoundException](./esentfilenotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexInUseException](./esentindexinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexNotFoundException](./esentindexnotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidBufferSizeException](./esentinvalidbuffersizeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLogDataSequenceException](./esentinvalidlogdatasequenceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentKeyDuplicateException](./esentkeyduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentKeyTruncatedException](./esentkeytruncatedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogFileSizeMismatchDatabasesConsistentException](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchDatabasesConsistentException](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLSNotSetException](./esentlsnotsetexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingFullBackupException](./esentmissingfullbackupexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMultiValuedDuplicateAfterTruncationException](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMultiValuedDuplicateException](./esentmultivaluedduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNoAttachmentsFailedIncrementalReseedException](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNoBackupException](./esentnobackupexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNoCurrentRecordException](./esentnocurrentrecordexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentObjectNotFoundException](./esentobjectnotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOSSnapshotNotAllowedException](./esentossnapshotnotallowedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordDeletedException](./esentrecorddeletedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordNotFoundException](./esentrecordnotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordTooBigException](./esentrecordtoobigexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordTooBigForBackwardCompatibilityException](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecoveredWithErrorsException](./esentrecoveredwitherrorsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecoveredWithoutUndoDatabasesConsistentException](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecoveredWithoutUndoException](./esentrecoveredwithoutundoexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRestoreInProgressException](./esentrestoreinprogressexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSeparatedLongValueException](./esentseparatedlongvalueexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSurrogateBackupInProgressException](./esentsurrogatebackupinprogressexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTableDuplicateException](./esenttableduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTableInUseException](./esenttableinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTestInjectionNotSupportedException](./esenttestinjectionnotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentWriteConflictException](./esentwriteconflictexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentWriteConflictPrimaryIndexException](./esentwriteconflictprimaryindexexception-class.md)