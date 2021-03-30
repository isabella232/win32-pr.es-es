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
# <a name="shim-database-types"></a><span data-ttu-id="34831-103">Tipos de bases de datos de Shim</span><span class="sxs-lookup"><span data-stu-id="34831-103">Shim Database Types</span></span>

<span data-ttu-id="34831-104">Representan los tipos para las bases de datos de correcciones de compatibilidad (shim) principales y personalizadas.</span><span class="sxs-lookup"><span data-stu-id="34831-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="34831-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="34831-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="34831-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="34831-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="34831-107"><dt>**SDB \_ BASE \_ de datos**</dt> <dt>0x80000000</dt> principal</span><span class="sxs-lookup"><span data-stu-id="34831-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="34831-108">La base de datos principal.</span><span class="sxs-lookup"><span data-stu-id="34831-108">The main database.</span></span> <span data-ttu-id="34831-109">Si este marcador no está presente, la base de datos es una base de datos personalizada.</span><span class="sxs-lookup"><span data-stu-id="34831-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="34831-110"><dt>**SDB \_ \_Corrección de compatibilidad de base de datos**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="34831-111">La base de datos contiene entradas de la aplicación que se corregido.</span><span class="sxs-lookup"><span data-stu-id="34831-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="34831-112"><dt>**SDB \_ BASE de datos \_ MSI**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="34831-113">La base de datos contiene entradas MSI.</span><span class="sxs-lookup"><span data-stu-id="34831-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="34831-114"><dt>**SDB \_ \_Controladores de base de datos**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="34831-115">La base de datos contiene entradas de bloque de controlador.</span><span class="sxs-lookup"><span data-stu-id="34831-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="34831-116"><dt>**SDB \_ \_Detalles**</dt> de la base de datos <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="34831-117">La base de datos contiene detalles de apphelp.</span><span class="sxs-lookup"><span data-stu-id="34831-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="34831-118"><dt>**SDB \_ \_ \_ Detalles de SP de base de datos**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="34831-119">La base de datos contiene detalles de SP apphelp.</span><span class="sxs-lookup"><span data-stu-id="34831-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="34831-120"><dt>**SDB \_ \_Recurso de base de datos**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="34831-121">La DLL de recursos contiene detalles de apphelp.</span><span class="sxs-lookup"><span data-stu-id="34831-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="34831-122"><dt>**SDB \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0xF02F0000</dt></span><span class="sxs-lookup"><span data-stu-id="34831-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="34831-123">Máscara que se usa para extraer la información de la base de datos principal.</span><span class="sxs-lookup"><span data-stu-id="34831-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="34831-124"><dt>**\_corrección de \_ compatibilidad principal de base de datos SDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34831-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="34831-125">SDB \_ Database \_ Shim \| SDB \_ Database \_ MSI \| \_ \_ base de datos Main</span><span class="sxs-lookup"><span data-stu-id="34831-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="34831-126"><dt>**\_MSI principal de base de datos SDB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34831-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="34831-127">base de datos SDB archivo. \_ \_ \| \_ \_</span><span class="sxs-lookup"><span data-stu-id="34831-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="34831-128"><dt>**\_ \_ controladores principales de la base de datos SDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34831-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="34831-129">SDB \_ Database drivers \_ \| SDB \_ \_ Main</span><span class="sxs-lookup"><span data-stu-id="34831-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="34831-130"><dt>**\_ \_ detalles principales de la base de datos SDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34831-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="34831-131">detalles de la base de datos SDB base de datos \_ \_ \| SDB \_ \_ principal</span><span class="sxs-lookup"><span data-stu-id="34831-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="34831-132"><dt>**\_ \_ detalles principales del \_ SP de la base de datos SDB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34831-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="34831-133">SDB \_ Database \_ Sp \_ Details \| SDB \_ Database \_ Main</span><span class="sxs-lookup"><span data-stu-id="34831-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="34831-134"><dt>**\_recurso principal de base de datos SDB \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34831-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="34831-135">\_recurso de base de datos SDB \_ \| \_ \_ principal</span><span class="sxs-lookup"><span data-stu-id="34831-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="34831-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34831-136">Requirements</span></span>



| <span data-ttu-id="34831-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="34831-137">Requirement</span></span> | <span data-ttu-id="34831-138">Value</span><span class="sxs-lookup"><span data-stu-id="34831-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="34831-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34831-139">Minimum supported client</span></span><br/> | <span data-ttu-id="34831-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34831-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="34831-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34831-141">Minimum supported server</span></span><br/> | <span data-ttu-id="34831-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="34831-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34831-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="34831-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34831-144">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="34831-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




