---
description: 'Más información sobre: Clase EsentInconsistentException'
title: Clase EsentInconsistentException
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60db39de93b448f6a655ed644460c0d16e5b27ad6132373efcf357fc986b16c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838325"
---
# <a name="esentinconsistentexception-class"></a>Clase EsentInconsistentException

Clase base para excepciones incoherentes.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentInconsistentException  
            

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentInconsistentException](./esentinconsistentexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentInconsistentException  
            [Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException](./esentattacheddatabasemismatchexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException](./esentbadcheckpointsignatureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException](./esentbadlogsignatureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadLogVersionException](./esentbadlogversionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException](./esentcheckpointfilenotfoundexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException](./esentconsistenttimemismatchexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException](./esentdatabasedirtyshutdownexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException](./esentdatabaselogsetmismatchexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException](./esentdbtimetoonewexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException](./esentdbtimetoooldexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException](./esentendingrestorelogtoolowexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException](./esentfileinvalidtypeexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException](./esentinvalidcreatedbversionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException](./esentinvaliddatabaseversionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException](./esentloggenerationmismatchexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException](./esentmissingcurrentlogfilesexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException](./esentmissingfiletobackupexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException](./esentmissingrestorelogfilesexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException](./esentpagesizemismatchexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException](./esentrequiredlogfilesmissingexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException](./esentstartingrestorelogtoohighexception-class.md)