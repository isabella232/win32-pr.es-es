---
title: EDB_RSTMAP estructura (Ntdsbcli. h)
description: Se usa con la función DsRestoreRegister para asignar una base de datos de copia de seguridad a una nueva base de datos.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- Estructura de EDB_RSTMAP Active Directory
- PEDB_RSTMAP puntero de estructura Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079489"
---
# <a name="edb_rstmap-structure"></a>\_Estructura RSTMAP de edb

La estructura **EDB \_ RSTMAP** se usa con la función [**DsRestoreRegister**](dsrestoreregister.md) para asignar una base de datos de copia de seguridad a una nueva base de datos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szDatabaseName**
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre de la base de datos cuando se hizo la copia de seguridad.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nuevo nombre de la base de datos, incluida su nueva ubicación, cuando sea aplicable.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **EDB \_ RSTMAPW** (Unicode) y **EDB \_ RSTMAPA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Estructuras de copia de seguridad de directorios](directory-backup-structures.md)
</dt> </dl>

 

 





