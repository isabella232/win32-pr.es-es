---
title: Estructura de CHANGE_LOG_ENTRY
description: Una entrada de registro de cambios.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- Restaurar sistema de estructura CHANGE_LOG_ENTRY
- PCHANGE_LOG_ENTRY de puntero de estructura para restaurar sistema
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079014"
---
# <a name="change_log_entry-structure"></a><span data-ttu-id="baa67-105">CAMBIAR \_ la \_ estructura de entrada del registro</span><span class="sxs-lookup"><span data-stu-id="baa67-105">CHANGE\_LOG\_ENTRY structure</span></span>

<span data-ttu-id="baa67-106">\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="baa67-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="baa67-107">Una entrada de registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="baa67-107">A change log entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa67-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baa67-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a><span data-ttu-id="baa67-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="baa67-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="baa67-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="baa67-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-111">Una estructura de [**\_ encabezado de registro**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="baa67-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="baa67-112">El miembro **dwRecordType** debe establecerse en **RecordTypeLogEntry** (1).</span><span class="sxs-lookup"><span data-stu-id="baa67-112">The **dwRecordType** member should be set to **RecordTypeLogEntry** (1).</span></span>

</dd> <dt>

<span data-ttu-id="baa67-113">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="baa67-113">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-114">Este miembro debe establecerse en 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="baa67-114">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="baa67-115">**dwEntryType**</span><span class="sxs-lookup"><span data-stu-id="baa67-115">**dwEntryType**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-116">Este miembro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="baa67-116">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

<span data-ttu-id="baa67-117">CHANGE \_ log \_ ENTRYTYPES \_ ACLCHANGE \* \* (0X2) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-117">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ACLCHANGE\*\* (0x2)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

<span data-ttu-id="baa67-118">CHANGE \_ log \_ ENTRYTYPES \_ ATTRCHANGE \* \* (0x4) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-118">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ATTRCHANGE\*\* (0x4)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

<span data-ttu-id="baa67-119">CHANGE \_ log \_ ENTRYTYPES \_ DIRCREATE \* \* (0x80) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-119">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRCREATE\*\* (0x80)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

<span data-ttu-id="baa67-120">CHANGE \_ log \_ ENTRYTYPES \_ DIRRENAME \* \* (0x100) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-120">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRRENAME\*\* (0x100)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

<span data-ttu-id="baa67-121">CHANGE \_ log \_ ENTRYTYPES \_ DIRDELETE \* \* (0x200) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-121">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRDELETE\*\* (0x200)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

<span data-ttu-id="baa67-122">CHANGE \_ log \_ ENTRYTYPES \_ FILECREATE \* \* (0x20) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-122">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILECREATE\*\* (0x20)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

<span data-ttu-id="baa67-123">CHANGE \_ log \_ ENTRYTYPES \_ FILEDELETE \* \* (0x10) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-123">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILEDELETE\*\* (0x10)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

<span data-ttu-id="baa67-124">CHANGE \_ log \_ ENTRYTYPES \_ FILERENAME \* \* (0x40) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-124">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILERENAME\*\* (0x40)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

<span data-ttu-id="baa67-125">CHANGE \_ log \_ ENTRYTYPES \_ INPRECREATE \* \* (0x100000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-125">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_INPRECREATE\*\* (0x100000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

<span data-ttu-id="baa67-126">CHANGE \_ log \_ ENTRYTYPES \_ ISDIR \* \* (0x20000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-126">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISDIR\*\* (0x20000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

<span data-ttu-id="baa67-127">CHANGE \_ log \_ ENTRYTYPES \_ ISNOTDIR \* \* (0x40000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-127">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISNOTDIR\*\* (0x40000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

<span data-ttu-id="baa67-128">CHANGE \_ log \_ ENTRYTYPES \_ MOUNTCREATE \* \* (0x400) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-128">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTCREATE\*\* (0x400)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

<span data-ttu-id="baa67-129">CHANGE \_ log \_ ENTRYTYPES \_ MOUNTDELETE \* \* (0x800) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-129">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTDELETE\*\* (0x800)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

<span data-ttu-id="baa67-130">ENTRYTYPES de registro de cambios \_ \_ \_ nooptimize \* \* (0x10000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-130">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_NOOPTIMIZE\*\* (0x10000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

<span data-ttu-id="baa67-131">CHANGE \_ log \_ ENTRYTYPES \_ OPENBYID \* \* (0x200000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-131">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_OPENBYID\*\* (0x200000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

<span data-ttu-id="baa67-132">CHANGE \_ log \_ ENTRYTYPES \_ SIMULATEDELETE \* \* (0x80000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-132">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_SIMULATEDELETE\*\* (0x80000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

<span data-ttu-id="baa67-133">CHANGE \_ log \_ ENTRYTYPES \_ STREAMCHANGE \* \* (0x1) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-133">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCHANGE\*\* (0x1)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

<span data-ttu-id="baa67-134">CHANGE \_ log \_ ENTRYTYPES \_ STREAMCREATE \* \* (0x2000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-134">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCREATE\*\* (0x2000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

<span data-ttu-id="baa67-135">CHANGE \_ log \_ ENTRYTYPES \_ STREAMOVERWRITE \* \* (0x8) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-135">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMOVERWRITE\*\* (0x8)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

<span data-ttu-id="baa67-136">CHANGE \_ log \_ ENTRYTYPES \_ VOLUMEERROR \* \* (0x1000) \* \*</span><span class="sxs-lookup"><span data-stu-id="baa67-136">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_VOLUMEERROR\*\* (0x1000)\*\*</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="baa67-137">**dwEntryFlags**</span><span class="sxs-lookup"><span data-stu-id="baa67-137">**dwEntryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-138">Este miembro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="baa67-138">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

<span data-ttu-id="baa67-139">**CHANGE \_ log \_ ENTRYFLAGS \_ ACLINFO (0x4)**</span><span class="sxs-lookup"><span data-stu-id="baa67-139">**CHANGE\_LOG\_ENTRYFLAGS\_ACLINFO (0x4)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

<span data-ttu-id="baa67-140">**CHANGE \_ log \_ ENTRYFLAGS \_ DEBUGINFO (0x8)**</span><span class="sxs-lookup"><span data-stu-id="baa67-140">**CHANGE\_LOG\_ENTRYFLAGS\_DEBUGINFO (0x8)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

<span data-ttu-id="baa67-141">**ENTRYFLAGS de registro de cambios \_ \_ \_ SECONDPATH (0X2)**</span><span class="sxs-lookup"><span data-stu-id="baa67-141">**CHANGE\_LOG\_ENTRYFLAGS\_SECONDPATH (0x2)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

<span data-ttu-id="baa67-142">**CHANGE \_ log \_ ENTRYFLAGS \_ nombre_corto (0x10)**</span><span class="sxs-lookup"><span data-stu-id="baa67-142">**CHANGE\_LOG\_ENTRYFLAGS\_SHORTNAME (0x10)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

<span data-ttu-id="baa67-143">**ENTRYFLAGS de registro de cambios \_ \_ \_ TempPath (0x1)**</span><span class="sxs-lookup"><span data-stu-id="baa67-143">**CHANGE\_LOG\_ENTRYFLAGS\_TEMPPATH (0x1)**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="baa67-144">**dwAttributes**</span><span class="sxs-lookup"><span data-stu-id="baa67-144">**dwAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-145">Atributos de archivo del archivo de registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="baa67-145">The file attributes of the change log file.</span></span> <span data-ttu-id="baa67-146">Si no se especifica ningún atributo, este valor debe establecerse en 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="baa67-146">If no attributes are specified, this value should be set to 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="baa67-147">**i64SequenceNum**</span><span class="sxs-lookup"><span data-stu-id="baa67-147">**i64SequenceNum**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-148">El número de secuencia asignado a la entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="baa67-148">The sequence number assigned to the change log entry.</span></span>

</dd> <dt>

<span data-ttu-id="baa67-149">**szProcName**</span><span class="sxs-lookup"><span data-stu-id="baa67-149">**szProcName**</span></span>
</dt> <dd>

<span data-ttu-id="baa67-150">Nombre del proceso que realiza el cambio.</span><span class="sxs-lookup"><span data-stu-id="baa67-150">The name of the process making the change.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="baa67-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baa67-151">Remarks</span></span>

<span data-ttu-id="baa67-152">Esta estructura va seguida de un número variable de registros de datos de longitud variable, más un valor **DWORD** que debe ser idéntico al valor del miembro **dwRecordSize** de **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="baa67-152">This structure is followed by a variable number of variable-length data records, plus a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

<span data-ttu-id="baa67-153">Los registros de datos de longitud variable se componen de una estructura de [**\_ encabezado de registro**](record-header.md) además de datos que se pueden utilizar para restaurar la entrada del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="baa67-153">The variable-length data records consist of a [**RECORD\_HEADER**](record-header.md) structure plus data that can be used to restore the change log entry.</span></span> <span data-ttu-id="baa67-154">El formato de los datos depende del valor del miembro **dwRecordType** de la estructura del **\_ encabezado del registro** .</span><span class="sxs-lookup"><span data-stu-id="baa67-154">The format of the data depends on the value of the **dwRecordType** member of the **RECORD\_HEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa67-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baa67-155">Requirements</span></span>



| <span data-ttu-id="baa67-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="baa67-156">Requirement</span></span> | <span data-ttu-id="baa67-157">Value</span><span class="sxs-lookup"><span data-stu-id="baa67-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="baa67-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baa67-158">Minimum supported client</span></span><br/> | <span data-ttu-id="baa67-159">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="baa67-159">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="baa67-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="baa67-160">Minimum supported server</span></span><br/> | <span data-ttu-id="baa67-161">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="baa67-161">None supported</span></span><br/>                            |
| <span data-ttu-id="baa67-162">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="baa67-162">End of client support</span></span><br/>    | <span data-ttu-id="baa67-163">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="baa67-163">Windows XP with SP2</span></span><br/>                       |



 

 





