---
title: WINBIO_STORAGE_SCHEMA estructura (Winbio \_ types.h)
description: Describe las funcionalidades de un adaptador de almacenamiento biométrico.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA estructura Windows API de marco biométrico
- PWINBIO_STORAGE_SCHEMA puntero de estructura Windows API de marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc0bd0d61814b4133c3789b0c8119edcaf79945452cc26aa313504c055ac2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909262"
---
# <a name="winbio_storage_schema-structure"></a>Estructura DE \_ ESQUEMA DE ALMACENAMIENTO DE \_ WINBIO

La **estructura DE ESQUEMA DE ALMACENAMIENTO \_ \_ DE WINBIO** describe las funcionalidades de un adaptador de almacenamiento biométrico. Esta estructura la usa la [**función WinBioEnumDatabases.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Tipo de medida biométrica guardada en la base de datos.

</dd> <dt>

**DatabaseId**
</dt> <dd>

GUID que identifica la base de datos.

</dd> <dt>

**DataFormat**
</dt> <dd>

GUID que identifica el formato de las plantillas de la base de datos.

</dd> <dt>

**Atributos**
</dt> <dd>

Información sobre las características de la base de datos. Puede ser un OR bit a **bit** de las siguientes constantes.



| Value                                                                                                                                                                                                                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ MÁSCARA \_ DE MARCA DE \_ BASE**</dt> <dt>DE DATOS 0xFFFF0000</dt> </dl>                | Representa una máscara para los bits de marca.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ MARCA \_ DE BASE DE DATOS \_ REMOTE**</dt> <dt>0x00020000</dt> </dl>          | La base de datos reside en un equipo remoto.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ MARCA \_ DE BASE DE DATOS \_ 0X00010000**</dt> <dt></dt> </dl> | La base de datos reside en una unidad extraíble.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | La base de datos se administra mediante un sistema de administración de bases de datos.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ FILE**</dt> <dt>0x00000001</dt> </dl>                | La base de datos está contenida en un archivo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ MÁSCARA \_ DE TIPO DE BASE \_ DE**</dt> <dt>DATOS 0x0000FFFF</dt> </dl>                | Representa una máscara para los bits de tipo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | La base de datos reside en el sensor biométrico.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ TARJETA**</dt> <dt>INTELIGENTE 0x00000004</dt> </dl> | La base de datos reside en una tarjeta inteligente.<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

Ruta de acceso y nombre de archivo de la base de datos si reside en el disco del equipo.

</dd> <dt>

**Connectionstring**
</dt> <dd>

Valor de cadena que se puede enviar a un servidor de bases de datos para identificar la base de datos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





