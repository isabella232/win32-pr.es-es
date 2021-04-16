---
description: Las clases WMI que representan archivos o directorios, como \_ CodecFile de Win32 o \_ archivo de información CIM, contienen una propiedad AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de derechos de acceso a archivos y directorios (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708249"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="936d0-103">Constantes de derechos de acceso a archivos y directorios</span><span class="sxs-lookup"><span data-stu-id="936d0-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="936d0-104">Las clases WMI que representan archivos o directorios, como [**\_ CodecFile de Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile) o [**\_ archivo**](/windows/desktop/CIMWin32Prov/cim-datafile)de información CIM, contienen una propiedad **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="936d0-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="936d0-105">Esta propiedad contiene valores de bit que especifican los derechos de acceso que debe tener un usuario o grupo para las operaciones o el acceso específico en el archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="936d0-106">Para obtener más información, consulte [derechos de acceso y seguridad de archivos](/windows/desktop/FileIO/file-security-and-access-rights) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="936d0-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="936d0-107">Las clases de archivo o directorio que contienen una propiedad **AccessMask** incluyen:</span><span class="sxs-lookup"><span data-stu-id="936d0-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="936d0-108">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="936d0-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="936d0-109">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="936d0-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="936d0-110">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="936d0-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="936d0-111">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="936d0-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="936d0-112">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="936d0-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="936d0-113">[**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="936d0-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="936d0-114">**\_Recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="936d0-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="936d0-115">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="936d0-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="936d0-116">En la lista siguiente se enumeran los valores de los derechos de acceso a archivos y directorios en la propiedad **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="936d0-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="936d0-117">Esta propiedad es un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="936d0-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="936d0-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_datos de lectura de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="936d0-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-120">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**directorio de la lista de archivos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="936d0-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-123">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="936d0-124">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="936d0-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_datos de escritura de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-126">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="936d0-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-127">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**ARCHIVO \_ agregar \_ archivo**</span><span class="sxs-lookup"><span data-stu-id="936d0-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-129">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="936d0-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-130">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="936d0-131">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="936d0-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**ARCHIVO \_ de \_ datos anexados**</span><span class="sxs-lookup"><span data-stu-id="936d0-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="936d0-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-134">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="936d0-135">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="936d0-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**\_agregar \_ subdirectorio de archivo**</span><span class="sxs-lookup"><span data-stu-id="936d0-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-137">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="936d0-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-138">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="936d0-139">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="936d0-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**ARCHIVO de \_ lectura \_ EA**</span><span class="sxs-lookup"><span data-stu-id="936d0-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-141">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="936d0-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-142">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="936d0-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**escritura de archivo \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="936d0-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-144">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="936d0-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-145">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="936d0-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_Ejecutar archivo**</span><span class="sxs-lookup"><span data-stu-id="936d0-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-147">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="936d0-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-148">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**recorrido de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-150">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="936d0-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-151">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-151">Grants the right to execute a file.</span></span> <span data-ttu-id="936d0-152">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="936d0-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**ARCHIVO- \_ eliminar \_ secundario**</span><span class="sxs-lookup"><span data-stu-id="936d0-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-154">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="936d0-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-155">Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="936d0-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_atributos de lectura de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-157">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="936d0-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-158">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_atributos de escritura de archivo \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="936d0-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-161">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="936d0-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-162"><span id="DELETE"></span><span id="delete"></span>**ELIMÍNELOS**</span><span class="sxs-lookup"><span data-stu-id="936d0-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-163">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="936d0-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-164">Concede el derecho para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="936d0-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**CONTROL de lectura \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-166">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="936d0-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-167">Concede el derecho para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL.</span><span class="sxs-lookup"><span data-stu-id="936d0-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**ESCRIBIR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="936d0-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-169">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="936d0-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-170">Concede el derecho a modificar la DACL en el descriptor de seguridad del objeto para el objeto.</span><span class="sxs-lookup"><span data-stu-id="936d0-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**propietario de escritura \_**</span><span class="sxs-lookup"><span data-stu-id="936d0-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-172">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="936d0-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-173">Concede el derecho a cambiar el propietario del descriptor de seguridad para el objeto.</span><span class="sxs-lookup"><span data-stu-id="936d0-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="936d0-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SINCRONIZÁNDOSE**</span><span class="sxs-lookup"><span data-stu-id="936d0-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936d0-175">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="936d0-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="936d0-176">Concede el derecho a usar el objeto para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="936d0-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="936d0-177">Esto permite que un proceso espere hasta que el objeto esté en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="936d0-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="936d0-178">Algunos tipos de objetos no admiten este derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="936d0-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="936d0-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="936d0-179">Requirements</span></span>



| <span data-ttu-id="936d0-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="936d0-180">Requirement</span></span> | <span data-ttu-id="936d0-181">Value</span><span class="sxs-lookup"><span data-stu-id="936d0-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="936d0-182">Encabezado</span><span class="sxs-lookup"><span data-stu-id="936d0-182">Header</span></span><br/> | <dl> <span data-ttu-id="936d0-183"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="936d0-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936d0-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="936d0-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936d0-185">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="936d0-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="936d0-186">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="936d0-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

