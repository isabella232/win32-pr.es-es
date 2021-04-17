---
description: Contiene el encabezado de la lista de revocación global (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Estructura de GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659779"
---
# <a name="grl_header-structure"></a>La \_ estructura del encabezado GRL

Contiene el encabezado de la lista de revocación global (GRL).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wszIdentifier**
</dt> <dd>

El identificador GRL. El valor siempre es L "MSGRL".

</dd> <dt>

**wFormatMajor**
</dt> <dd>

Número de versión principal. Actualmente, el valor debe ser 1.

</dd> <dt>

**wFormatMinor**
</dt> <dd>

Número de versión secundaria. Actualmente, el valor debe ser cero.

</dd> <dt>

**CreationTime**
</dt> <dd>

Un valor de **FILETIME** que especifica cuándo se creó el archivo.

</dd> <dt>

**dwSequenceNumber**
</dt> <dd>

Número de versión de GRL. Actualmente, el valor debe ser al menos 3.

</dd> <dt>

**dwForceRebootVersion**
</dt> <dd>

Reservado.

</dd> <dt>

**dwForceProcessRestartVersion**
</dt> <dd>

Reservado.

</dd> <dt>

**cbRevocationSectionOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio del GRL hasta la sección principal.

</dd> <dt>

**cRevokedKernelBinaries**
</dt> <dd>

El número de archivos binarios de kernel revocados que aparecen en el GRL.

</dd> <dt>

**cRevokedUserBinaries**
</dt> <dd>

El número de archivos binarios de modo de usuario revocados que aparecen en el GRL.

</dd> <dt>

**cRevokedCertificates**
</dt> <dd>

El número de certificados revocados que aparecen en el GRL.

</dd> <dt>

**cTrustedRoots**
</dt> <dd>

El número de raíces de confianza enumeradas en el GRL.

</dd> <dt>

**cbExtensibleSectionOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio del GRL hasta la sección extensible.

</dd> <dt>

**cExtensibleEntries**
</dt> <dd>

El número de entradas en la sección extensible.

</dd> <dt>

**cbRenewalSectionOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio del GRL hasta la sección de renovación.

</dd> <dt>

**cRevokedKernelBinaryRenewals**
</dt> <dd>

El número de renovaciones binarias del kernel enumeradas en el GRL.

</dd> <dt>

**cRevokedUserBinaryRenewals**
</dt> <dd>

El número de renovaciones binarias de modo de usuario enumeradas en el GRL.

</dd> <dt>

**cRevokedCertificateRenewals**
</dt> <dd>

El número de renovaciones de certificado enumeradas en el GRL.

</dd> <dt>

**cbSignatureCoreOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio del GRL hasta la firma de la sección principal.

</dd> <dt>

**cbSignatureExtOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio del GRL hasta la firma de la sección extensible.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todos los enteros del GRL tienen un orden de bytes Little-Endian. Todas las estructuras se alinean con límites de 1 byte.

Esta estructura no se declara en un encabezado de SDK. Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Revocación de certificados OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estructuras OPM](opm-structures.md)
</dt> </dl>

 

 




