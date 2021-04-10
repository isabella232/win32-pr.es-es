---
description: Representa un registro de atributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Estructura de ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906965"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="b4c39-103">Estructura del encabezado del \_ registro de atributos \_</span><span class="sxs-lookup"><span data-stu-id="b4c39-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="b4c39-104">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="b4c39-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="b4c39-105">Representa un registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c39-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4c39-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="b4c39-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4c39-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4c39-108">**TypeCode**</span><span class="sxs-lookup"><span data-stu-id="b4c39-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-109">Código de tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-109">The attribute type code.</span></span>



| <span data-ttu-id="b4c39-110">Value</span><span class="sxs-lookup"><span data-stu-id="b4c39-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="b4c39-111">Significado</span><span class="sxs-lookup"><span data-stu-id="b4c39-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="b4c39-112"><dt>**$Standard \_ INFORMACIÓN**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="b4c39-113">Atributos de archivo (como de solo lectura y archivo), marcas de tiempo (por ejemplo, creación de archivos y última modificación) y el número de vínculos físicos.</span><span class="sxs-lookup"><span data-stu-id="b4c39-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="b4c39-114"><dt>**$Attribute \_ ENUMERAr**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="b4c39-115">Una lista de atributos que constituyen el archivo y la referencia de archivo del registro de archivo MFT en el que se encuentra cada atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="b4c39-116"><dt>**$File \_ NOMBRE**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="b4c39-117">Nombre del archivo, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="b4c39-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="b4c39-118"><dt>**$Object \_ ID.**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="b4c39-119">Identificador de objeto de 64 bytes asignado por el servicio de seguimiento de vínculos.</span><span class="sxs-lookup"><span data-stu-id="b4c39-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="b4c39-120"><dt>**$Volume \_ NOMBRE**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="b4c39-121">Etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="b4c39-121">The volume label.</span></span> <span data-ttu-id="b4c39-122">Presente en el archivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="b4c39-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="b4c39-123"><dt>**$Volume \_**</dt> <dt>0X70</dt> de información</span><span class="sxs-lookup"><span data-stu-id="b4c39-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="b4c39-124">Información del volumen.</span><span class="sxs-lookup"><span data-stu-id="b4c39-124">The volume information.</span></span> <span data-ttu-id="b4c39-125">Presente en el archivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="b4c39-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="b4c39-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="b4c39-127">Contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="b4c39-128"><dt>**$Index \_**</dt> <dt>0x90</dt> raíz</span><span class="sxs-lookup"><span data-stu-id="b4c39-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="b4c39-129">Se usa para implementar la asignación de nombres de archivo para directorios grandes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="b4c39-130"><dt>**$Index \_**</dt> <dt>0XA0</dt> de asignación</span><span class="sxs-lookup"><span data-stu-id="b4c39-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="b4c39-131">Se usa para implementar la asignación de nombres de archivo para directorios grandes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="b4c39-132"><dt>**$Bitmap**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="b4c39-133">Índice de mapa de bits para un directorio grande.</span><span class="sxs-lookup"><span data-stu-id="b4c39-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="b4c39-134"><dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="b4c39-135">Los datos del punto de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="b4c39-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="b4c39-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="b4c39-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-137">Tamaño del registro de atributo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="b4c39-138">Este valor refleja el tamaño necesario para la variante de registro y siempre se redondea al límite de quadword más próximo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-139">**FormCode**</span><span class="sxs-lookup"><span data-stu-id="b4c39-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-140">Código del formulario de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-140">The attribute form code.</span></span>



| <span data-ttu-id="b4c39-141">Value</span><span class="sxs-lookup"><span data-stu-id="b4c39-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="b4c39-142">Significado</span><span class="sxs-lookup"><span data-stu-id="b4c39-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="b4c39-143"><dt>**Residente \_ de FORMULARIO**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="b4c39-144">El valor se encuentra en el registro de archivo y sigue inmediatamente al encabezado del registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="b4c39-145">No <dt>**residente \_ FORMULARIO**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="b4c39-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="b4c39-146">El valor está contenido en otros sectores del disco.</span><span class="sxs-lookup"><span data-stu-id="b4c39-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="b4c39-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="b4c39-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-148">Tamaño del nombre del atributo opcional, en caracteres, o 0 si no hay ningún nombre de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="b4c39-149">La longitud máxima del nombre del atributo es de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b4c39-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-150">**NameOffset**</span><span class="sxs-lookup"><span data-stu-id="b4c39-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-151">Desplazamiento del nombre del atributo desde el inicio del registro del atributo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="b4c39-152">Si el miembro **NameLength** es 0, este miembro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b4c39-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-153">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="b4c39-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-154">Marcas de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="b4c39-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Atributo \_ de \_ \_ Máscara de compresión de marca** (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="b4c39-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="b4c39-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Atributo \_ de MARCA \_ Sparse** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="b4c39-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="b4c39-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Atributo \_ de MARCA \_ cifrada** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="b4c39-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b4c39-158">**Instancia**</span><span class="sxs-lookup"><span data-stu-id="b4c39-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-159">Instancia única para este atributo en el registro de archivo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-160">**Forma**</span><span class="sxs-lookup"><span data-stu-id="b4c39-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-161">Si el miembro **FormCode** es \_ un formulario residente, la Unión es una estructura **residente** .</span><span class="sxs-lookup"><span data-stu-id="b4c39-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="b4c39-162">Si **FormCode** es \_ un formulario no residente, la Unión es una estructura no **residente** .</span><span class="sxs-lookup"><span data-stu-id="b4c39-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="b4c39-163">**LaserPrep**</span><span class="sxs-lookup"><span data-stu-id="b4c39-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4c39-164">**ValueLength**</span><span class="sxs-lookup"><span data-stu-id="b4c39-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-165">Tamaño del valor del atributo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-166">**ValueOffset**</span><span class="sxs-lookup"><span data-stu-id="b4c39-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-167">Desplazamiento al valor desde el inicio del registro de atributo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-168">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b4c39-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-169">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b4c39-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b4c39-170">**No residente**</span><span class="sxs-lookup"><span data-stu-id="b4c39-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4c39-171">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="b4c39-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-172">El número de clúster virtual más bajo (VCN) incluido en este registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-173">**HighestVcn**</span><span class="sxs-lookup"><span data-stu-id="b4c39-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-174">El valor VCN más alto incluido en este registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-175">**MappingPairsOffset**</span><span class="sxs-lookup"><span data-stu-id="b4c39-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-176">El desplazamiento a la asignación empareja la matriz desde el inicio del registro del atributo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="b4c39-177">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b4c39-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-178">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b4c39-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-179">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b4c39-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-180">**AllocatedLength**</span><span class="sxs-lookup"><span data-stu-id="b4c39-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-181">Tamaño asignado del archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="b4c39-182">Este valor es un múltiplo par del tamaño del clúster.</span><span class="sxs-lookup"><span data-stu-id="b4c39-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="b4c39-183">Este miembro no es válido si el miembro **LowestVcn** es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b4c39-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-184">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="b4c39-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-185">Tamaño del archivo (byte más alto que se puede leer más 1), en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="b4c39-186">Este miembro no es válido si **LowestVcn** es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b4c39-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-187">**ValidDataLength**</span><span class="sxs-lookup"><span data-stu-id="b4c39-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-188">La longitud de datos válida (byte inicializado más alto más 1), en bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c39-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="b4c39-189">Este valor se redondea al límite del clúster más próximo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="b4c39-190">Este miembro no es válido si **LowestVcn** es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b4c39-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="b4c39-191">**TotalAllocated**</span><span class="sxs-lookup"><span data-stu-id="b4c39-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="b4c39-192">El total asignado para el archivo (la suma de los clústeres asignados).</span><span class="sxs-lookup"><span data-stu-id="b4c39-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4c39-193">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4c39-193">Remarks</span></span>

<span data-ttu-id="b4c39-194">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="b4c39-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="b4c39-195">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="b4c39-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="b4c39-196">Los registros de atributos siempre están alineados en un límite quadword.</span><span class="sxs-lookup"><span data-stu-id="b4c39-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="b4c39-197">Si el atributo no es residente, el encabezado del registro de atributo contiene una lista de información de recuperación que proporciona una asignación entre VCN y el número de clúster lógico (LCN) para el atributo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="b4c39-198">Si la información de recuperación no cabe en el segmento de archivo base, puede almacenarse en un segmento de registro de archivo externo.</span><span class="sxs-lookup"><span data-stu-id="b4c39-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="b4c39-199">Si todavía no cabe en un segmento de registro de archivo externo, hay una disposición en la lista de atributos para que contenga varias entradas para un atributo que requiera información de recuperación adicional.</span><span class="sxs-lookup"><span data-stu-id="b4c39-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="b4c39-200">La matriz de pares de asignación se almacena en un formato comprimido y presupone que el sistema descomprime y almacena en caché la información.</span><span class="sxs-lookup"><span data-stu-id="b4c39-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="b4c39-201">Consta de una serie de pares NextVcn/CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="b4c39-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="b4c39-202">Por ejemplo, si un archivo tiene una sola ejecución de 8 clústeres a partir de LCN 128 y el archivo se inicia en LowestVcn 0, la matriz de pares de asignación tiene una sola entrada, que es NextVcn = 8 y CurrentLcn = 128.</span><span class="sxs-lookup"><span data-stu-id="b4c39-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="b4c39-203">La matriz es una secuencia de bytes que almacena los cambios en las variables de trabajo cuando se procesa secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="b4c39-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="b4c39-204">El flujo de bytes se va a interpretar como una secuencia terminada en cero de triples, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b4c39-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="b4c39-205">recuento de bytes = *v* + (*l* \* 16)</span><span class="sxs-lookup"><span data-stu-id="b4c39-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="b4c39-206">donde *v* es el número de bytes de VCN de orden inferior modificados y *l* es el número de bytes de LCN de orden inferior modificados.</span><span class="sxs-lookup"><span data-stu-id="b4c39-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="b4c39-207">El algoritmo de descompresión es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b4c39-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="b4c39-208">Inicialice NextVcn en `Attribute->LowestVcn` y CurrentLcn en 0.</span><span class="sxs-lookup"><span data-stu-id="b4c39-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="b4c39-209">Inicialice el puntero de secuencia de bytes a `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .</span><span class="sxs-lookup"><span data-stu-id="b4c39-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="b4c39-210">Establezca CurrentVcn en NextVcn.</span><span class="sxs-lookup"><span data-stu-id="b4c39-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="b4c39-211">Lee el siguiente byte de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b4c39-211">Read the next byte from the stream.</span></span> <span data-ttu-id="b4c39-212">Si es 0, interrumpa; en caso contrario, extraiga *v* y *l* como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b4c39-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="b4c39-213">Interprete los siguientes *v* bytes como una cantidad firmada, con el byte de orden inferior en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="b4c39-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="b4c39-214">Desempaquete Sign-Extended en 64 bits y agréguelo a NextVcn.</span><span class="sxs-lookup"><span data-stu-id="b4c39-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="b4c39-215">Interprete los siguientes bytes de *l* como una cantidad firmada, con el byte de orden inferior en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="b4c39-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="b4c39-216">Desempaquete Sign-Extended en 64 bits y agréguelo a CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="b4c39-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="b4c39-217">Si esto produce un CurrentLcn de 0, el valor de VCNs de CurrentVcn a NextVcn-1 no está asignado.</span><span class="sxs-lookup"><span data-stu-id="b4c39-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="b4c39-218">Actualice la información de asignación almacenada en caché desde CurrentVcn, NextVcn y CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="b4c39-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="b4c39-219">Vaya al paso 3.</span><span class="sxs-lookup"><span data-stu-id="b4c39-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4c39-220">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4c39-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c39-221">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="b4c39-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
