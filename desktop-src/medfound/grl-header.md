---
description: Contiene el encabezado de lista de revocación global (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: GRL_HEADER estructura
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
ms.openlocfilehash: 59e2435395db59ae1ee5ae0bf200ef4d004c2f056546af7d40e33c1adc741b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063457"
---
# <a name="grl_header-structure"></a>Estructura GRL \_ HEADER

Contiene el encabezado de lista de revocación global (GRL).

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

Identificador GRL. El valor es siempre L"MSGRL".

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

Valor **FILETIME** que especifica cuándo se creó el archivo.

</dd> <dt>

**dwSequenceNumber**
</dt> <dd>

Número de versión grl. Actualmente, el valor debe ser al menos 3.

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

Desplazamiento, en bytes, desde el inicio de la GRL hasta la sección Core.

</dd> <dt>

**cRevokedKernelBinaries**
</dt> <dd>

Número de binarios de kernel revocados enumerados en la GRL.

</dd> <dt>

**cRevokedUserBinaries**
</dt> <dd>

Número de archivos binarios en modo de usuario revocados enumerados en la GRL.

</dd> <dt>

**cRevokedCertificates**
</dt> <dd>

Número de certificados revocados enumerados en la GRL.

</dd> <dt>

**cTrustedRoots**
</dt> <dd>

Número de raíces de confianza enumeradas en la GRL.

</dd> <dt>

**cbExtensibleSectionOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio de grl hasta la sección Extensible.

</dd> <dt>

**cExtensibleEntries**
</dt> <dd>

Número de entradas de la sección Extensible.

</dd> <dt>

**cbRenewalSectionOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio de la GRL hasta la sección Renovaciones.

</dd> <dt>

**cRevokedKernelBinaryRenewals**
</dt> <dd>

Número de renovaciones binarias de kernel enumeradas en la GRL.

</dd> <dt>

**cRevokedUserBinaryRenewals**
</dt> <dd>

Número de renovaciones binarias en modo de usuario enumeradas en la GRL.

</dd> <dt>

**cRevokedCertificateRenewals**
</dt> <dd>

Número de renovaciones de certificados enumeradas en la GRL.

</dd> <dt>

**cbSignatureCoreOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio de la GRL hasta la firma de la sección Core.

</dd> <dt>

**cbSignatureExtOffset**
</dt> <dd>

Desplazamiento, en bytes, desde el inicio de grl hasta la firma de sección extensible.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Todos los enteros de la GRL tienen una ordenación de bytes little-endian. Todas las estructuras se alinean con límites de 1 byte.

Esta estructura no se declara en un encabezado sdk. Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Revocación de certificados de OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estructuras de OPM](opm-structures.md)
</dt> </dl>

 

 




