---
description: Representa el segmento de registro de archivo. Este es el encabezado de cada segmento de registro de archivo de la tabla de archivos maestra (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Estructura de FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274847"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="c2683-104">\_Estructura de \_ encabezado de segmento de registro de archivo \_</span><span class="sxs-lookup"><span data-stu-id="c2683-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="c2683-105">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="c2683-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="c2683-106">Representa el segmento de registro de archivo.</span><span class="sxs-lookup"><span data-stu-id="c2683-106">Represents the file record segment.</span></span> <span data-ttu-id="c2683-107">Este es el encabezado de cada segmento de registro de archivo de la tabla de archivos maestra (MFT).</span><span class="sxs-lookup"><span data-stu-id="c2683-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2683-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2683-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="c2683-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2683-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2683-110">**MultiSectorHeader**</span><span class="sxs-lookup"><span data-stu-id="c2683-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-111">Encabezado de multisector definido por el administrador de caché.</span><span class="sxs-lookup"><span data-stu-id="c2683-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="c2683-112">La estructura de [**\_ \_ encabezado de varios sectores**](multi-sector-header.md) siempre contiene la firma "archivo" y una descripción de la ubicación y el tamaño de la matriz de la secuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="c2683-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="c2683-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2683-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c2683-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-116">El número de secuencia global.</span><span class="sxs-lookup"><span data-stu-id="c2683-116">The sequence number.</span></span> <span data-ttu-id="c2683-117">Este valor se incrementa cada vez que se libera un segmento de registro de archivo; es 0 si no se utiliza el segmento.</span><span class="sxs-lookup"><span data-stu-id="c2683-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="c2683-118">El campo **SequenceNumber** de una referencia de archivo debe coincidir con el contenido de este campo; Si no coinciden, la referencia de archivo es incorrecta y probablemente está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="c2683-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-119">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="c2683-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2683-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-121">**FirstAttributeOffset**</span><span class="sxs-lookup"><span data-stu-id="c2683-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-122">Desplazamiento del primer registro de atributo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c2683-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-123">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="c2683-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-124">Marcas de archivo.</span><span class="sxs-lookup"><span data-stu-id="c2683-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="c2683-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Archivo \_ de \_Segmento \_ de registro en \_ uso** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="c2683-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="c2683-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Archivo \_ de Índice de nombre de archivo \_ \_ \_ presente** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="c2683-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="c2683-127">**Reserved3**</span><span class="sxs-lookup"><span data-stu-id="c2683-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2683-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-129">**BaseFileRecordSegment**</span><span class="sxs-lookup"><span data-stu-id="c2683-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-130">Referencia de archivo al segmento de registro de archivo base para este archivo.</span><span class="sxs-lookup"><span data-stu-id="c2683-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="c2683-131">Si este es el registro del archivo base, el valor es 0.</span><span class="sxs-lookup"><span data-stu-id="c2683-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="c2683-132">Consulte [**\_ \_ referencia de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c2683-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2683-133">**Reserved4**</span><span class="sxs-lookup"><span data-stu-id="c2683-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-134">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c2683-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c2683-135">**UpdateSequenceArray**</span><span class="sxs-lookup"><span data-stu-id="c2683-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="c2683-136">La matriz de secuencias de actualización para proteger las transferencias multisector del segmento de registro de archivos.</span><span class="sxs-lookup"><span data-stu-id="c2683-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2683-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2683-137">Remarks</span></span>

<span data-ttu-id="c2683-138">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="c2683-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="c2683-139">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="c2683-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="c2683-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2683-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2683-141">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="c2683-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
