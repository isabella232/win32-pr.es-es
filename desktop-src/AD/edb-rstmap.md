---
title: EDB_RSTMAP estructura (Ntdsbcli.h)
description: Se usa con la función DsRestoreRegister para asignar una base de datos de copia de seguridad a una nueva base de datos.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP estructura Active Directory
- PEDB_RSTMAP de puntero de estructura Active Directory
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
ms.openlocfilehash: 1c81fe35d8d41818d279df094a57c041b8ea52212d2ce2f0cdc379628f5d5971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191696"
---
# <a name="edb_rstmap-structure"></a>Estructura \_ RSTMAP de EDB

La **estructura \_ RSTMAP** de EDB se usa con la función [**DsRestoreRegister**](dsrestoreregister.md) para asignar una base de datos de copia de seguridad a una nueva base de datos.

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

Puntero a una cadena terminada en NULL que contiene el nombre de la base de datos en la que se ha hecho una copia de seguridad.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nuevo nombre de la base de datos, incluida su nueva ubicación, cuando corresponda.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **EDB \_ RSTMAPW** (Unicode) y **EDB \_ RSTMAPA** (ANSI)<br/>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Estructuras de copia de seguridad de directorios](directory-backup-structures.md)
</dt> </dl>

 

 





