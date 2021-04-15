---
title: Estructura de WINBIO_STORAGE_SCHEMA (Winbio \_ Types. h)
description: Describe las capacidades de un adaptador de almacenamiento biométrico.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- Plataforma de biometría de Windows API de WINBIO_STORAGE_SCHEMA Structure
- PWINBIO_STORAGE_SCHEMA de puntero de estructura Plataforma de biometría de Windows API
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
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666077"
---
# <a name="winbio_storage_schema-structure"></a>WINBIO \_ estructura de esquema de almacenamiento \_

La estructura de **\_ \_ esquema de almacenamiento WINBIO** describe las capacidades de un adaptador de almacenamiento biométrico. La función [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) usa esta estructura.

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

GUID que identifica el formato de las plantillas en la base de datos.

</dd> <dt>

**Atributos**
</dt> <dd>

Información acerca de las características de la base de datos. Puede ser **una operación OR bit a bit** de las siguientes constantes.



| Value                                                                                                                                                                                                                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de marca de base de datos**</dt> <dt>0xFFFF0000</dt> </dl>                | Representa una máscara para los bits de marcador.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ Marca de base de datos 0x00020000 \_ \_ remoto**</dt> <dt></dt> </dl>          | La base de datos reside en un equipo remoto.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ Marca de base de datos 0x00010000 \_ \_ extraíble**</dt> <dt></dt> </dl> | La base de datos reside en una unidad extraíble.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ Tipo de base de datos \_ \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | La base de datos se administra mediante un sistema de administración de bases de datos.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ Archivo de tipo de base de datos**</dt> <dt>0x00000001</dt> </dl>                | La base de datos se encuentra en un archivo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0x0000FFFF</dt> </dl>                | Representa una máscara para los bits de tipo.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ Tipo de base de datos en el \_ \_ chip**</dt> <dt>0x00000003</dt> </dl>          | La base de datos reside en el sensor biométrico.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ Tipo de base de datos \_ \_ SmartCard**</dt> <dt>0x00000004</dt> </dl> | La base de datos reside en una tarjeta inteligente.<br/>                    |



 

</dd> <dt>

**FilePath**
</dt> <dd>

La ruta de acceso y el nombre de archivo de la base de datos si reside en el disco del equipo.

</dd> <dt>

**ConnectionString**
</dt> <dd>

Valor de cadena que se puede enviar a un servidor de base de datos para identificar la base de datos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





