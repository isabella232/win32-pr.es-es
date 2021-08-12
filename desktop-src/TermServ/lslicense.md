---
title: LSLicense (estructura)
description: Contiene información sobre una licencia de Servicios de Escritorio remoto específica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- LSLicense structure Servicios de Escritorio remoto
- Puntero de estructura LPLSLicense Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ea276b1b1217505a7bb44e1d70dd58d53eb57933d755ed9f79100abc177c3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605418"
---
# <a name="lslicense-structure"></a>LSLicense (estructura)

Contiene información sobre una licencia de Servicios de Escritorio remoto específica.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Versión de la licencia.

</dd> <dt>

**dwLicenseId**
</dt> <dd>

Identificador de la licencia.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

Identificador del [**LSKeyPack**](lskeypack.md) que contiene la licencia.

</dd> <dt>

**szHWID**
</dt> <dd>

Identificador de hardware del Conexión a Escritorio remoto cliente de Conexión a Escritorio remoto (RDC) que se emitió la licencia.

</dd> <dt>

**szMachineName**
</dt> <dd>

Nombre del cliente Conexión a Escritorio remoto (RDC) que se emitió la licencia.

</dd> <dt>

**szUserName**
</dt> <dd>

Nombre del usuario al que se emitió la licencia.

</dd> <dt>

**dwCertSerialLicense**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**dwLicenseSerialNumber**
</dt> <dd>

Número de serie de la licencia.

</dd> <dt>

**ftIssueDate**
</dt> <dd>

Fecha en que se emitió la licencia.

</dd> <dt>

**ftExpireDate**
</dt> <dd>

Fecha en que expirará la licencia.

</dd> <dt>

**ucLicenseStatus**
</dt> <dd>

Estado actual de la licencia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

 





