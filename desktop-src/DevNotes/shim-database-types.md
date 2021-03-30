---
description: Representan los tipos para las bases de datos de correcciones de compatibilidad (shim) principales y personalizadas.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Tipos de bases de datos de Shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806907"
---
# <a name="shim-database-types"></a>Tipos de bases de datos de Shim

Representan los tipos para las bases de datos de correcciones de compatibilidad (shim) principales y personalizadas.



| Constante o valor                                                                                                                                                                                                                                                | Descripción                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ BASE \_ de datos**</dt> <dt>0x80000000</dt> principal </dl>                    | La base de datos principal. Si este marcador no está presente, la base de datos es una base de datos personalizada.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ \_Corrección de compatibilidad de base de datos**</dt> <dt>0x00010000</dt> </dl>                    | La base de datos contiene entradas de la aplicación que se corregido.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ BASE de datos \_ MSI**</dt> <dt>0x00020000</dt> </dl>                       | La base de datos contiene entradas MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ \_Controladores de base de datos**</dt> <dt>0x00040000</dt> </dl>           | La base de datos contiene entradas de bloque de controlador.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ \_Detalles**</dt> de la base de datos <dt>0x00080000</dt> </dl>           | La base de datos contiene detalles de apphelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ \_ \_ Detalles de SP de base de datos**</dt> <dt>0x00100000</dt> </dl> | La base de datos contiene detalles de SP apphelp.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ \_Recurso de base de datos**</dt> <dt>0x00200000</dt> </dl>        | La DLL de recursos contiene detalles de apphelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0xF02F0000</dt> </dl>    | Máscara que se usa para extraer la información de la base de datos principal.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**\_corrección de \_ compatibilidad principal de base de datos SDB \_**</dt> </dl>                                                                    | SDB \_ Database \_ Shim \| SDB \_ Database \_ MSI \| \_ \_ base de datos Main<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**\_MSI principal de base de datos SDB \_ \_**</dt> </dl>                                                                       | base de datos SDB archivo. \_ \_ \| \_ \_<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**\_ \_ controladores principales de la base de datos SDB \_**</dt> </dl>                                                           | SDB \_ Database drivers \_ \| SDB \_ \_ Main<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_ \_ detalles principales de la base de datos SDB \_**</dt> </dl>                                                           | detalles de la base de datos SDB base de datos \_ \_ \| SDB \_ \_ principal<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**\_ \_ detalles principales del \_ SP de la base de datos SDB \_**</dt> </dl>                                                 | SDB \_ Database \_ Sp \_ Details \| SDB \_ Database \_ Main<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_recurso principal de base de datos SDB \_ \_**</dt> </dl>                                                        | \_recurso de base de datos SDB \_ \| \_ \_ principal<br/>                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




