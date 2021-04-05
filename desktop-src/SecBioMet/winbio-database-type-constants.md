---
title: Constantes de WINBIO_DATABASE_TYPE (Winbio \_ Types. h)
description: Marcas que se pueden usar para el miembro Attributes de la \_ estructura de esquema de almacenamiento WINBIO \_ .
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802294"
---
# <a name="winbio_database_type-constants"></a>\_Constantes de tipo de base de datos WINBIO \_

Las marcas siguientes se pueden usar para el miembro **attributes** de la estructura del [**\_ \_ esquema de almacenamiento WINBIO**](winbio-storage-schema.md) .



| Constante o valor                                                                                                                                                                                                                                                                     | Descripción                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0x0000FFFF</dt> </dl>                | Representa una máscara para todos los \_ bits de tipo \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ Archivo de tipo de base de datos**</dt> <dt>0x00000001</dt> </dl>                | La base de datos se encuentra en un archivo.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ Tipo de base de datos \_ \_ DBMS**</dt> <dt>0x00000002</dt> </dl>                | La base de datos se administra mediante un componente externo del sistema de administración de bases de datos (DBMS), como Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ Tipo de base de datos en el \_ \_ chip**</dt> <dt>0x00000003</dt> </dl>          | La base de datos reside en el sensor biométrico.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ Tipo de base de datos \_ \_ SmartCard**</dt> <dt>0x00000004</dt> </dl> | La base de datos reside en una tarjeta inteligente.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Máscara de marca de base de datos**</dt> <dt>0xFFFF0000</dt> </dl>                | Representa una máscara para todos los \_ bits de marca \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ Marca de base de datos 0x00010000 \_ \_ extraíble**</dt> <dt></dt> </dl> | El medio de almacenamiento que contiene la base de datos se puede quitar físicamente del equipo.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ Marca de base de datos 0x00020000 \_ \_ remoto**</dt> <dt></dt> </dl>          | La base de datos reside en un equipo remoto.<br/>                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





