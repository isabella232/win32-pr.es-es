---
description: 'Más información sobre: Clase EsentCorruptionException'
title: Clase EsentCorruptionException
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963311"
---
# <a name="esentcorruptionexception-class"></a>Clase EsentCorruptionException

Clase base para excepciones corruption.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentCorruptionException  
            

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Miembros de EsentCorruptionException](./esentcorruptionexception-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipos derivados

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentCorruptionException  
            [Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException](./esentbademptypageexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadPageLinkException](./esentbadpagelinkexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException](./esentbadparentpagelinkexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException](./esentcatalogcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException](./esentcheckpointcorruptexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException](./esentdatabasecorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException](./esentdbtimecorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException](./esentdecompressionfailedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException](./esentfileiobeyondeofexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogCorruptedException](./esentlogcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException](./esentlogfilecorruptexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLVCorruptedException](./esentlvcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingLogFileException](./esentmissinglogfileexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException](./esentpagenotinitializedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException](./esentreadverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException](./esentredoabruptendedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException](./esentspavailextcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException](./esentspownextcorruptedexception-class.md)