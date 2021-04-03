---
description: Representa una entrada en la lista de atributos.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Estructura de ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906966"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="469e8-103">Estructura de entrada de \_ lista de atributos \_</span><span class="sxs-lookup"><span data-stu-id="469e8-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="469e8-104">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="469e8-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="469e8-105">Representa una entrada en la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="469e8-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="469e8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="469e8-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="469e8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="469e8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="469e8-108">**AttributeTypeCode**</span><span class="sxs-lookup"><span data-stu-id="469e8-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-109">Código de tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="469e8-109">The attribute type code.</span></span>



| <span data-ttu-id="469e8-110">Value</span><span class="sxs-lookup"><span data-stu-id="469e8-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="469e8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="469e8-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="469e8-112"><dt>**$Standard \_ INFORMACIÓN**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="469e8-113">Atributos de archivo (como de solo lectura y archivo), marcas de tiempo (por ejemplo, creación de archivos y última modificación) y el número de vínculos físicos.</span><span class="sxs-lookup"><span data-stu-id="469e8-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="469e8-114"><dt>**$Attribute \_ ENUMERAr**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="469e8-115">Una lista de atributos que constituyen el archivo y la referencia de archivo del registro de archivo MFT en el que se encuentra cada atributo.</span><span class="sxs-lookup"><span data-stu-id="469e8-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="469e8-116"><dt>**$File \_ NOMBRE**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="469e8-117">Nombre del archivo, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="469e8-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="469e8-118"><dt>**$Object \_ ID.**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="469e8-119">Identificador de objeto de 16 bytes asignado por el servicio de seguimiento de vínculos.</span><span class="sxs-lookup"><span data-stu-id="469e8-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="469e8-120"><dt>**$Volume \_ NOMBRE**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="469e8-121">Etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="469e8-121">The volume label.</span></span> <span data-ttu-id="469e8-122">Presente en el archivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="469e8-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="469e8-123"><dt>**$Volume \_**</dt> <dt>0X70</dt> de información</span><span class="sxs-lookup"><span data-stu-id="469e8-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="469e8-124">Información del volumen.</span><span class="sxs-lookup"><span data-stu-id="469e8-124">The volume information.</span></span> <span data-ttu-id="469e8-125">Presente en el archivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="469e8-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="469e8-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="469e8-127">Contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="469e8-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="469e8-128"><dt>**$Index \_**</dt> <dt>0x90</dt> raíz</span><span class="sxs-lookup"><span data-stu-id="469e8-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="469e8-129">Se usa para implementar la asignación de nombres de archivo para directorios grandes.</span><span class="sxs-lookup"><span data-stu-id="469e8-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="469e8-130"><dt>**$Index \_**</dt> <dt>0XA0</dt> de asignación</span><span class="sxs-lookup"><span data-stu-id="469e8-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="469e8-131">Se usa para implementar la asignación de nombres de archivo para directorios grandes.</span><span class="sxs-lookup"><span data-stu-id="469e8-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="469e8-132"><dt>**$Bitmap**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="469e8-133">Índice de mapa de bits para un directorio grande.</span><span class="sxs-lookup"><span data-stu-id="469e8-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="469e8-134"><dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="469e8-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="469e8-135">Los datos del punto de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="469e8-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="469e8-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="469e8-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-137">Tamaño de esta estructura, más el búfer de nombres opcional, en bytes.</span><span class="sxs-lookup"><span data-stu-id="469e8-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="469e8-138">**AttributeNameLength**</span><span class="sxs-lookup"><span data-stu-id="469e8-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-139">Tamaño del nombre del atributo opcional, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="469e8-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="469e8-140">Si existe un nombre, este valor es distinto de cero y la estructura va seguida inmediatamente de una cadena Unicode del número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="469e8-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="469e8-141">**AttributeNameOffset**</span><span class="sxs-lookup"><span data-stu-id="469e8-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="469e8-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="469e8-143">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="469e8-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-144">El número de clúster virtual más bajo (VCN) para este atributo.</span><span class="sxs-lookup"><span data-stu-id="469e8-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="469e8-145">Este miembro es cero a menos que el atributo requiera varios segmentos de registro de archivos y a menos que esta entrada sea una referencia a un segmento que no sea el primero.</span><span class="sxs-lookup"><span data-stu-id="469e8-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="469e8-146">En este caso, este valor es el VCN más bajo descrito por el segmento al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="469e8-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="469e8-147">**SegmentReference**</span><span class="sxs-lookup"><span data-stu-id="469e8-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-148">El segmento de la tabla de archivos maestros (MFT) en el que reside el atributo.</span><span class="sxs-lookup"><span data-stu-id="469e8-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="469e8-149">Consulte [**\_ \_ referencia de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="469e8-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="469e8-150">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="469e8-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-151">Reservado.</span><span class="sxs-lookup"><span data-stu-id="469e8-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="469e8-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="469e8-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="469e8-153">Inicio del nombre del atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="469e8-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="469e8-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="469e8-154">Remarks</span></span>

<span data-ttu-id="469e8-155">La lista de atributos es una lista ordenada de estructuras de **\_ \_ entradas de lista de atributos** alineados quadword.</span><span class="sxs-lookup"><span data-stu-id="469e8-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="469e8-156">Esta lista se ordena primero por el código de tipo de atributo y, a continuación, por el nombre del atributo (si está presente).</span><span class="sxs-lookup"><span data-stu-id="469e8-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="469e8-157">Dos atributos no pueden tener el mismo código de tipo, nombre y VCN más bajo.</span><span class="sxs-lookup"><span data-stu-id="469e8-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="469e8-158">Por lo tanto, puede haber como máximo un atributo para cada código de tipo sin nombre.</span><span class="sxs-lookup"><span data-stu-id="469e8-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="469e8-159">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="469e8-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="469e8-160">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="469e8-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="469e8-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="469e8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469e8-162">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="469e8-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
