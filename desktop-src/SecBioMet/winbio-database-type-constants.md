---
title: WINBIO_DATABASE_TYPE constantes (Winbio \_ types.h)
description: Marcas que se pueden usar para el miembro Attributes de la estructura DE ESQUEMA \_ DE ALMACENAMIENTO \_ DE WINBIO.
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160770"
---
# <a name="winbio_database_type-constants"></a>Constantes DE \_ TIPO DE BASE DE DATOS \_ WINBIO

Las marcas siguientes se pueden usar para el miembro **Attributes** de la [**estructura DE ESQUEMA DE ALMACENAMIENTO \_ \_ DE WINBIO.**](winbio-storage-schema.md)



| Constante o valor                                                                                                                                                                                                                                                                     | Descripción                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ MASK**</dt> <dt>0x0000FFFF</dt> </dl>                | Representa una máscara para todos los \_ \_ bits TYPE.<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ FILE**</dt> <dt>0x00000001</dt> </dl>                | La base de datos está contenida en un archivo.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ BASE \_ DE DATOS DE TIPO \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | La base de datos se administra mediante un componente del sistema de administración de bases de datos (DBMS) externo, como Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | La base de datos reside en el sensor biométrico.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ TIPO \_ DE BASE DE DATOS \_ TARJETA**</dt> <dt>INTELIGENTE 0x00000004</dt> </dl> | La base de datos reside en una tarjeta inteligente.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ MÁSCARA \_ DE MARCA DE BASE \_ DE**</dt> <dt>DATOS 0xFFFF0000</dt> </dl>                | Representa una máscara para todos los \_ \_ bits FLAG.<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ MARCA \_ DE BASE DE \_ DATOS 0X00010000**</dt> <dt></dt> </dl> | El medio de almacenamiento que contiene la base de datos se puede quitar físicamente del equipo.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ MARCA \_ DE BASE DE DATOS \_ REMOTE**</dt> <dt>0x00020000</dt> </dl>          | La base de datos reside en un equipo remoto.<br/>                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





