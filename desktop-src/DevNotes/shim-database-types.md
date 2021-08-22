---
description: Representa los tipos de bases de datos de correcciones de compatibilidad (shim) principales y personalizadas.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipos de base de datos shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cc36cbb198570618fbd1a6524e4e7c6dc6812fb01bd74fe04cf1bd91b31f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075929"
---
# <a name="shim-database-types"></a>Tipos de base de datos shim

Representa los tipos de bases de datos de correcciones de compatibilidad (shim) principales y personalizadas.



| Constante o valor                                                                                                                                                                                                                                                | Descripción                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ Base \_ de datos principal**</dt> <dt>0x80000000</dt> </dl>                    | Base de datos principal. Si esta marca no está presente, la base de datos es una base de datos personalizada.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ Compatibilidad con \_ correcciones de compatibilidad (SHIM)**</dt> <dt>de base de datos 0x00010000</dt> </dl>                    | La base de datos contiene las entradas de la aplicación que se deben recortar.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ Base \_ de datos MSI**</dt> <dt>0x00020000</dt> </dl>                       | La base de datos contiene entradas MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ Controladores \_ de base**</dt> de datos <dt>0x00040000</dt> </dl>           | La base de datos contiene entradas de bloque de controladores.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ Detalles \_ de la base**</dt> de datos <dt>0x00080000</dt> </dl>           | La base de datos contiene los detalles de Apphelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ DATABASE \_ SP \_ DETAILS**</dt> <dt>0x00100000</dt> </dl> | La base de datos contiene detalles de SP Apphelp.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ Database \_ RESOURCE**</dt> <dt>0x00200000</dt> </dl>        | El archivo DLL de recursos contiene los detalles de Apphelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ MÁSCARA \_ DE TIPO \_ DE**</dt> <dt>BASE DE DATOS 0xF02F0000</dt> </dl>    | Máscara que se usa para extraer la información principal de la base de datos.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**CORRECCIÓN DE COMPATIBILIDAD \_ \_ (SHIM) PRINCIPAL DE LA BASE DE DATOS \_ SDB**</dt> </dl>                                                                    | SDB \_ DATABASE \_ SHIM \| SDB \_ DATABASE \_ MSI \| SDB \_ DATABASE \_ MAIN<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ MSI**</dt> </dl>                                                                       | SDB \_ DATABASE \_ MSI \| SDB \_ DATABASE \_ MAIN<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**CONTROLADORES PRINCIPALES DE BASE \_ DE \_ DATOS SDB \_**</dt> </dl>                                                           | SDB \_ DATABASE \_ DRIVERS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**DETALLES PRINCIPALES DE LA \_ BASE \_ DE DATOS SDB \_**</dt> </dl>                                                           | SDB \_ DATABASE \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**DETALLES DEL SP PRINCIPAL DE LA \_ \_ BASE DE DATOS \_ DE \_ SDB**</dt> </dl>                                                 | SDB \_ DATABASE \_ SP \_ DETAILS \| SDB \_ DATABASE \_ MAIN<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**RECURSO PRINCIPAL DE \_ BASE DE \_ DATOS \_ SDB**</dt> </dl>                                                        | SDB \_ DATABASE \_ RESOURCE \| SDB \_ DATABASE \_ MAIN<br/>                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




