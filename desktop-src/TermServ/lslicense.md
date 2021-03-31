---
title: Estructura LSLicense
description: Contiene información acerca de una licencia de Servicios de Escritorio remoto específica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la estructura LSLicense
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
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490331"
---
# <a name="lslicense-structure"></a>Estructura LSLicense

Contiene información acerca de una licencia de Servicios de Escritorio remoto específica.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

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

IDENTIFICADOR de la licencia.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

IDENTIFICADOR del [**LSKeyPack**](lskeypack.md) que contiene la licencia.

</dd> <dt>

**szHWID**
</dt> <dd>

IDENTIFICADOR de hardware del cliente de Conexión a Escritorio remoto (RDC) que emitió la licencia.

</dd> <dt>

**szMachineName**
</dt> <dd>

Nombre del cliente de Conexión a Escritorio remoto (RDC) que emitió la licencia.

</dd> <dt>

**szUserName**
</dt> <dd>

Nombre del usuario que emitió la licencia.

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

 

 





