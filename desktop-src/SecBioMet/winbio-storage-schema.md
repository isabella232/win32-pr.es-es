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
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="f526e-105">WINBIO \_ estructura de esquema de almacenamiento \_</span><span class="sxs-lookup"><span data-stu-id="f526e-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="f526e-106">La estructura de **\_ \_ esquema de almacenamiento WINBIO** describe las capacidades de un adaptador de almacenamiento biométrico.</span><span class="sxs-lookup"><span data-stu-id="f526e-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="f526e-107">La función [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="f526e-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f526e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f526e-108">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="f526e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f526e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f526e-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="f526e-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="f526e-111">Tipo de medida biométrica guardada en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f526e-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="f526e-112">**DatabaseId**</span><span class="sxs-lookup"><span data-stu-id="f526e-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="f526e-113">GUID que identifica la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f526e-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="f526e-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="f526e-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="f526e-115">GUID que identifica el formato de las plantillas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f526e-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="f526e-116">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="f526e-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="f526e-117">Información acerca de las características de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f526e-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="f526e-118">Puede ser **una operación OR bit a bit** de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="f526e-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="f526e-119">Value</span><span class="sxs-lookup"><span data-stu-id="f526e-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="f526e-120">Significado</span><span class="sxs-lookup"><span data-stu-id="f526e-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="f526e-121"><dt>**WINBIO \_ \_ \_ Máscara de marca de base de datos**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="f526e-122">Representa una máscara para los bits de marcador.</span><span class="sxs-lookup"><span data-stu-id="f526e-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="f526e-123"><dt>**WINBIO \_ Marca de base de datos 0x00020000 \_ \_ remoto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f526e-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="f526e-124">La base de datos reside en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="f526e-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="f526e-125"><dt>**WINBIO \_ Marca de base de datos 0x00010000 \_ \_ extraíble**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f526e-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="f526e-126">La base de datos reside en una unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="f526e-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="f526e-127"><dt>**WINBIO \_ Tipo de base de datos \_ \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="f526e-128">La base de datos se administra mediante un sistema de administración de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="f526e-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="f526e-129"><dt>**WINBIO \_ \_ \_ Archivo de tipo de base de datos**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="f526e-130">La base de datos se encuentra en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f526e-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="f526e-131"><dt>**WINBIO \_ \_ \_ Máscara de tipo de base de datos**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="f526e-132">Representa una máscara para los bits de tipo.</span><span class="sxs-lookup"><span data-stu-id="f526e-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="f526e-133"><dt>**WINBIO \_ Tipo de base de datos en el \_ \_ chip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="f526e-134">La base de datos reside en el sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="f526e-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="f526e-135"><dt>**WINBIO \_ Tipo de base de datos \_ \_ SmartCard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="f526e-136">La base de datos reside en una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="f526e-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="f526e-137">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="f526e-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="f526e-138">La ruta de acceso y el nombre de archivo de la base de datos si reside en el disco del equipo.</span><span class="sxs-lookup"><span data-stu-id="f526e-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="f526e-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="f526e-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="f526e-140">Valor de cadena que se puede enviar a un servidor de base de datos para identificar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f526e-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f526e-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f526e-141">Requirements</span></span>



| <span data-ttu-id="f526e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f526e-142">Requirement</span></span> | <span data-ttu-id="f526e-143">Value</span><span class="sxs-lookup"><span data-stu-id="f526e-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f526e-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f526e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f526e-145">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f526e-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f526e-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f526e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f526e-147">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f526e-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f526e-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f526e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f526e-149"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f526e-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f526e-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f526e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f526e-151">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="f526e-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="f526e-152">**WinBioEnumDatabases**</span><span class="sxs-lookup"><span data-stu-id="f526e-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





