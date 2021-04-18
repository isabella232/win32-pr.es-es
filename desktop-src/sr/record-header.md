---
title: Estructura de RECORD_HEADER
description: Encabezado de registro usado por la entrada del registro de cambios \_ y las estructuras de encabezado del registro de \_ cambios \_ \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Restaurar sistema de estructura RECORD_HEADER
- PRECORD_HEADER de puntero de estructura para restaurar sistema
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492184"
---
# <a name="record_header-structure"></a><span data-ttu-id="484e2-105">Estructura del encabezado de registro \_</span><span class="sxs-lookup"><span data-stu-id="484e2-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="484e2-106">\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="484e2-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="484e2-107">Encabezado de registro usado por la [**\_ \_ entrada del registro de cambios**](change-log-entry.md) y las estructuras de [**\_ \_ encabezado del registro de cambios**](change-log-header.md) .</span><span class="sxs-lookup"><span data-stu-id="484e2-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="484e2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="484e2-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="484e2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="484e2-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="484e2-110">**dwRecordSize**</span><span class="sxs-lookup"><span data-stu-id="484e2-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="484e2-111">Tamaño total del registro, incluido el encabezado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="484e2-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="484e2-112">**dwRecordType**</span><span class="sxs-lookup"><span data-stu-id="484e2-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="484e2-113">Tipo de registro.</span><span class="sxs-lookup"><span data-stu-id="484e2-113">The record type.</span></span> <span data-ttu-id="484e2-114">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="484e2-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="484e2-115">Value</span><span class="sxs-lookup"><span data-stu-id="484e2-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="484e2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="484e2-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="484e2-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="484e2-118">El registro es el encabezado del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="484e2-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="484e2-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="484e2-120">El registro es el encabezado de una entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="484e2-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="484e2-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="484e2-122">Los datos son la ruta de acceso del volumen para la entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="484e2-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="484e2-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="484e2-124">Los datos son la ruta de acceso de archivo para la entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="484e2-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="484e2-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="484e2-126">Los datos se utilizan al cambiar el nombre de las entradas del registro de cambios; Esta ruta de acceso es donde se almacena el archivo cuyo nombre ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="484e2-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="484e2-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="484e2-128">Los datos son el nombre del archivo de copia de seguridad que se usa para restaurar la entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="484e2-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="484e2-129">Los archivos de copia de seguridad se encuentran en la carpeta RP *n* .</span><span class="sxs-lookup"><span data-stu-id="484e2-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="484e2-130">El nombre de archivo tiene el formato siguiente: un *xxxxxxx*. *ext*, donde *xxxxxxx* es un número de siete dígitos y *ext* es la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="484e2-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="484e2-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="484e2-132">Los datos son una ACL.</span><span class="sxs-lookup"><span data-stu-id="484e2-132">The data is an ACL.</span></span> <span data-ttu-id="484e2-133">El formato de los datos es una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="484e2-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="484e2-134">Este valor no puede ser mayor que 8.192 bytes.</span><span class="sxs-lookup"><span data-stu-id="484e2-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="484e2-135">Para especificar un valor mayor que 8.192 bytes, utilice el miembro **RecordTypeAclFile** .</span><span class="sxs-lookup"><span data-stu-id="484e2-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="484e2-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="484e2-137">Los datos son el nombre del archivo ACL utilizado para almacenar la ACL.</span><span class="sxs-lookup"><span data-stu-id="484e2-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="484e2-138">Los archivos ACL se encuentran en la carpeta RP *n* .</span><span class="sxs-lookup"><span data-stu-id="484e2-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="484e2-139">El nombre de archivo tiene el formato siguiente: S *xxxxxxx*. ACL, donde *xxxxxxx* es un número de siete dígitos.</span><span class="sxs-lookup"><span data-stu-id="484e2-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="484e2-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="484e2-141">Los datos son información de depuración para la entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="484e2-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="484e2-142">El formato de datos es una estructura de **\_ \_ \_ información de depuración de registro de Sr** .</span><span class="sxs-lookup"><span data-stu-id="484e2-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="484e2-143">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="484e2-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="484e2-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="484e2-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="484e2-145">Los datos son el nombre corto del archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="484e2-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="484e2-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="484e2-146">Remarks</span></span>

<span data-ttu-id="484e2-147">La estructura de **\_ \_ \_ información de depuración del registro de Sr** se define de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="484e2-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="484e2-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="484e2-148">Requirements</span></span>



| <span data-ttu-id="484e2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="484e2-149">Requirement</span></span> | <span data-ttu-id="484e2-150">Value</span><span class="sxs-lookup"><span data-stu-id="484e2-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="484e2-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="484e2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="484e2-152">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="484e2-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="484e2-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="484e2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="484e2-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="484e2-154">None supported</span></span><br/>                            |
| <span data-ttu-id="484e2-155">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="484e2-155">End of client support</span></span><br/>    | <span data-ttu-id="484e2-156">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="484e2-156">Windows XP with SP2</span></span><br/>                       |



 

