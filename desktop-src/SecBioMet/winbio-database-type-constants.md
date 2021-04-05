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
# <a name="winbio_database_type-constants"></a><span data-ttu-id="e9367-103">\_Constantes de tipo de base de datos WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="e9367-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="e9367-104">Las marcas siguientes se pueden usar para el miembro **attributes** de la estructura del [**\_ \_ esquema de almacenamiento WINBIO**](winbio-storage-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="e9367-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="e9367-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="e9367-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="e9367-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9367-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="e9367-107"><dt>**WINBIO \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="e9367-108">Representa una máscara para todos los \_ bits de tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="e9367-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="e9367-109"><dt>**WINBIO \_ \_ \_ Archivo de tipo de base de datos**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="e9367-110">La base de datos se encuentra en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e9367-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="e9367-111"><dt>**WINBIO \_ Tipo de base de datos \_ \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="e9367-112">La base de datos se administra mediante un componente externo del sistema de administración de bases de datos (DBMS), como Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9367-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="e9367-113"><dt>**WINBIO \_ Tipo de base de datos en el \_ \_ chip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="e9367-114">La base de datos reside en el sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="e9367-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="e9367-115"><dt>**WINBIO \_ Tipo de base de datos \_ \_ SmartCard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="e9367-116">La base de datos reside en una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e9367-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="e9367-117"><dt>**WINBIO \_ \_ \_ Máscara de marca de base de datos**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="e9367-118">Representa una máscara para todos los \_ bits de marca \_ .</span><span class="sxs-lookup"><span data-stu-id="e9367-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="e9367-119"><dt>**WINBIO \_ Marca de base de datos 0x00010000 \_ \_ extraíble**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e9367-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="e9367-120">El medio de almacenamiento que contiene la base de datos se puede quitar físicamente del equipo.</span><span class="sxs-lookup"><span data-stu-id="e9367-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="e9367-121"><dt>**WINBIO \_ Marca de base de datos 0x00020000 \_ \_ remoto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e9367-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="e9367-122">La base de datos reside en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e9367-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="e9367-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9367-123">Requirements</span></span>



| <span data-ttu-id="e9367-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9367-124">Requirement</span></span> | <span data-ttu-id="e9367-125">Value</span><span class="sxs-lookup"><span data-stu-id="e9367-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9367-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9367-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e9367-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9367-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e9367-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9367-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e9367-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9367-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e9367-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9367-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9367-131"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9367-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9367-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9367-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9367-133">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="e9367-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





