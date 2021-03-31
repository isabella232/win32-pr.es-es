---
description: Representa una conexión de red activa en un entorno basado en Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Win32_NetworkConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807832"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="a294e-103">\_Clase Win32 NetworkConnection</span><span class="sxs-lookup"><span data-stu-id="a294e-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="a294e-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection de Win32** representa una conexión de red activa en un entorno basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="a294e-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="a294e-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a294e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a294e-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a294e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a294e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a294e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="a294e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a294e-108">Members</span></span>

<span data-ttu-id="a294e-109">La **clase \_ NetworkConnection de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a294e-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="a294e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a294e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a294e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a294e-111">Properties</span></span>

<span data-ttu-id="a294e-112">La **clase \_ NetworkConnection de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a294e-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a294e-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="a294e-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a294e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-116">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a294e-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-117">Lista de derechos de acceso al archivo o directorio especificado que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia.</span><span class="sxs-lookup"><span data-stu-id="a294e-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="a294e-118">En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.</span><span class="sxs-lookup"><span data-stu-id="a294e-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a294e-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="a294e-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-120">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="a294e-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="a294e-121">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="a294e-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="a294e-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="a294e-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-123">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a294e-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="a294e-124">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="a294e-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="a294e-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Archivo \_ de ANEXAr \_ datos (archivo) o \_ \_ subdirectorio de adición de archivo** (4)</span><span class="sxs-lookup"><span data-stu-id="a294e-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-126">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="a294e-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="a294e-127">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="a294e-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="a294e-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="a294e-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-129">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="a294e-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="a294e-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="a294e-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-131">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="a294e-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="a294e-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="a294e-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-133">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="a294e-133">Grants the right to execute a file.</span></span> <span data-ttu-id="a294e-134">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="a294e-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="a294e-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="a294e-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-136">Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a294e-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="a294e-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="a294e-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-138">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="a294e-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="a294e-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="a294e-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-140">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="a294e-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="a294e-141"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="a294e-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-142">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="a294e-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="a294e-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="a294e-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-144">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="a294e-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="a294e-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="a294e-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-146">Concede acceso de escritura a la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="a294e-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="a294e-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="a294e-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-148">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="a294e-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="a294e-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="a294e-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="a294e-150">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="a294e-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a294e-151">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a294e-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-154">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a294e-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-155">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a294e-155">A short textual description of the object.</span></span>

<span data-ttu-id="a294e-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a294e-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a294e-157">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a294e-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-160">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")</span><span class="sxs-lookup"><span data-stu-id="a294e-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-161">Comentario proporcionado por el proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="a294e-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="a294e-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-165">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**use \_ info \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ status**")</span><span class="sxs-lookup"><span data-stu-id="a294e-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-166">Estado actual de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="a294e-167">**Conectado** ("conectado")</span><span class="sxs-lookup"><span data-stu-id="a294e-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a294e-168">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a294e-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a294e-169">En **pausa** ("en pausa")</span><span class="sxs-lookup"><span data-stu-id="a294e-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="a294e-170">**Desconectada** ("desconectada")</span><span class="sxs-lookup"><span data-stu-id="a294e-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="a294e-171">**Conectando** ("conectando")</span><span class="sxs-lookup"><span data-stu-id="a294e-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="a294e-172">**Volver a conectar** ("reconectar")</span><span class="sxs-lookup"><span data-stu-id="a294e-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a294e-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="a294e-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-176">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")</span><span class="sxs-lookup"><span data-stu-id="a294e-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-177">Tipo de persistencia de la conexión utilizada para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="a294e-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="a294e-178">**Conexión actual** ("conexión actual")</span><span class="sxs-lookup"><span data-stu-id="a294e-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="a294e-179">**Conexión persistente** ("conexión persistente")</span><span class="sxs-lookup"><span data-stu-id="a294e-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a294e-180">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a294e-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-183">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a294e-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-184">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a294e-184">A textual description of the object.</span></span>

<span data-ttu-id="a294e-185">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a294e-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a294e-186">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="a294e-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-189">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")</span><span class="sxs-lookup"><span data-stu-id="a294e-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-190">El objeto de red debe mostrarse en una interfaz de usuario de exploración de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="a294e-191">**Dominio** ("dominio")</span><span class="sxs-lookup"><span data-stu-id="a294e-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="a294e-192">**Generic** ("Generic")</span><span class="sxs-lookup"><span data-stu-id="a294e-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="a294e-193">**Servidor** ("servidor")</span><span class="sxs-lookup"><span data-stu-id="a294e-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="a294e-194">**Compartir** ("compartir")</span><span class="sxs-lookup"><span data-stu-id="a294e-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a294e-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a294e-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-196">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a294e-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-198">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a294e-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-199">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a294e-199">Indicates when the object was installed.</span></span> <span data-ttu-id="a294e-200">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="a294e-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a294e-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a294e-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a294e-202">**LocalName**</span><span class="sxs-lookup"><span data-stu-id="a294e-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-205">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")</span><span class="sxs-lookup"><span data-stu-id="a294e-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-206">Nombre local del dispositivo de red conectado.</span><span class="sxs-lookup"><span data-stu-id="a294e-206">Local name of the connected network device.</span></span>

<span data-ttu-id="a294e-207">Ejemplo: "c: \\ Public"</span><span class="sxs-lookup"><span data-stu-id="a294e-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="a294e-208">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a294e-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-211">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("nombre"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span><span class="sxs-lookup"><span data-stu-id="a294e-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-212">Nombre de la conexión de red actual.</span><span class="sxs-lookup"><span data-stu-id="a294e-212">Name of the current network connection.</span></span> <span data-ttu-id="a294e-213">Es la combinación de los valores de **RemoteName** y **localname**.</span><span class="sxs-lookup"><span data-stu-id="a294e-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="a294e-214">Ejemplo: " \\ \\ NTRELEASE (c: \\ Public)"</span><span class="sxs-lookup"><span data-stu-id="a294e-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="a294e-215">**Persistent**</span><span class="sxs-lookup"><span data-stu-id="a294e-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-216">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a294e-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-218">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| funciones de red de Windows \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span><span class="sxs-lookup"><span data-stu-id="a294e-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-219">El sistema operativo volverá a conectar automáticamente la conexión en el siguiente inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a294e-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="a294e-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="a294e-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-223">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")</span><span class="sxs-lookup"><span data-stu-id="a294e-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-224">Nombre del proveedor que posee el recurso.</span><span class="sxs-lookup"><span data-stu-id="a294e-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="a294e-225">Esta propiedad puede ser **null** si se desconoce el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a294e-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="a294e-226">**RemoteName**</span><span class="sxs-lookup"><span data-stu-id="a294e-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-229">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="a294e-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-230">Nombre de recurso de red remota para un recurso de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="a294e-231">Para una conexión actual o persistente, **RemoteName** contiene el nombre de red asociado al nombre del valor en la propiedad **localname** .</span><span class="sxs-lookup"><span data-stu-id="a294e-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="a294e-232">El nombre de **RemoteName** debe seguir las convenciones de nomenclatura del proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="a294e-233">Ejemplo: " \\ \\ NTRELEASE"</span><span class="sxs-lookup"><span data-stu-id="a294e-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="a294e-234">**RemotePath**</span><span class="sxs-lookup"><span data-stu-id="a294e-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-237">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="a294e-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-238">Ruta de acceso completa al recurso de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-238">Full path to the network resource.</span></span>

<span data-ttu-id="a294e-239">Ejemplo: " \\ \\ infosrv1 \\ Public"</span><span class="sxs-lookup"><span data-stu-id="a294e-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="a294e-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a294e-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-243">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")</span><span class="sxs-lookup"><span data-stu-id="a294e-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-244">Tipo de recurso que se va a enumerar o al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="a294e-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="a294e-245">**Disco** ("disco")</span><span class="sxs-lookup"><span data-stu-id="a294e-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="a294e-246">**Imprimir** ("Imprimir")</span><span class="sxs-lookup"><span data-stu-id="a294e-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="a294e-247">**Any** ("any")</span><span class="sxs-lookup"><span data-stu-id="a294e-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a294e-248">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a294e-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-251">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a294e-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-252">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a294e-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="a294e-253">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="a294e-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a294e-254">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="a294e-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a294e-255">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="a294e-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a294e-256">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a294e-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a294e-257">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a294e-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a294e-258">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a294e-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a294e-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a294e-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a294e-260">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a294e-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a294e-261">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a294e-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a294e-262">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a294e-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a294e-263">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a294e-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a294e-264">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a294e-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a294e-265">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a294e-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a294e-266">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a294e-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a294e-267">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a294e-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a294e-268">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a294e-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a294e-269">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a294e-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a294e-270">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a294e-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a294e-271">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a294e-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a294e-272">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a294e-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a294e-273">**UserName**</span><span class="sxs-lookup"><span data-stu-id="a294e-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a294e-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a294e-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a294e-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a294e-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a294e-276">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| funciones de red de Windows \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span><span class="sxs-lookup"><span data-stu-id="a294e-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="a294e-277">Nombre de usuario o nombre de usuario predeterminado que se usa para establecer una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="a294e-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="a294e-278">Ejemplo: "SYSTEM"</span><span class="sxs-lookup"><span data-stu-id="a294e-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a294e-279">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a294e-279">Remarks</span></span>

<span data-ttu-id="a294e-280">La **clase \_ NetworkConnection de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a294e-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a294e-281">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a294e-281">Examples</span></span>

<span data-ttu-id="a294e-282">El siguiente ejemplo de código de VBScript recupera información sobre la conexión de red local.</span><span class="sxs-lookup"><span data-stu-id="a294e-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="a294e-283">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a294e-283">Requirements</span></span>



| <span data-ttu-id="a294e-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="a294e-284">Requirement</span></span> | <span data-ttu-id="a294e-285">Value</span><span class="sxs-lookup"><span data-stu-id="a294e-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a294e-286">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a294e-286">Minimum supported client</span></span><br/> | <span data-ttu-id="a294e-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a294e-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a294e-288">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a294e-288">Minimum supported server</span></span><br/> | <span data-ttu-id="a294e-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a294e-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a294e-290">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a294e-290">Namespace</span></span><br/>                | <span data-ttu-id="a294e-291">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a294e-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a294e-292">MOF</span><span class="sxs-lookup"><span data-stu-id="a294e-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a294e-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a294e-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a294e-294">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a294e-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a294e-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a294e-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a294e-296">Vea también</span><span class="sxs-lookup"><span data-stu-id="a294e-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a294e-297">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a294e-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="a294e-298">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a294e-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
