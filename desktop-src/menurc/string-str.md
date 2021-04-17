---
title: Estructura de cadena
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de propiedad intelectual o sus marcas comerciales.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menús de estructura de cadena y otros recursos
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695884"
---
# <a name="string-structure"></a><span data-ttu-id="90e02-105">Estructura de cadena</span><span class="sxs-lookup"><span data-stu-id="90e02-105">String structure</span></span>

<span data-ttu-id="90e02-106">Representa la organización de los datos en un recurso de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="90e02-107">Contiene una cadena que describe un aspecto específico de un archivo, por ejemplo, la versión de un archivo, sus avisos de propiedad intelectual o sus marcas comerciales.</span><span class="sxs-lookup"><span data-stu-id="90e02-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e02-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90e02-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="90e02-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="90e02-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="90e02-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="90e02-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="90e02-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="90e02-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90e02-112">Longitud, en bytes, de esta estructura de **cadena** .</span><span class="sxs-lookup"><span data-stu-id="90e02-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="90e02-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="90e02-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="90e02-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="90e02-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90e02-115">Tamaño, en palabras, del miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="90e02-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="90e02-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="90e02-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="90e02-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="90e02-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90e02-118">El tipo de datos del recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="90e02-118">The type of data in the version resource.</span></span> <span data-ttu-id="90e02-119">Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="90e02-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="90e02-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="90e02-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="90e02-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="90e02-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="90e02-122">Cadena Unicode arbitraria.</span><span class="sxs-lookup"><span data-stu-id="90e02-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="90e02-123">El miembro **szKey** puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="90e02-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="90e02-124">Estos valores solo son instrucciones.</span><span class="sxs-lookup"><span data-stu-id="90e02-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="90e02-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Opiniones**</span><span class="sxs-lookup"><span data-stu-id="90e02-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-126">El miembro **Value** contiene cualquier información adicional que se debe mostrar con fines de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="90e02-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="90e02-127">Esta cadena puede ser una longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="90e02-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="90e02-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Compañía**</span><span class="sxs-lookup"><span data-stu-id="90e02-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-129">El miembro de **valor** identifica la compañía que generó el archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="90e02-130">Por ejemplo, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="90e02-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="90e02-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="90e02-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-132">El miembro **Value** describe el archivo de tal forma que se puede presentar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="90e02-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="90e02-133">Esta cadena se puede presentar en un cuadro de lista cuando el usuario elige los archivos que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="90e02-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="90e02-134">Por ejemplo, "controlador de teclado para teclados de estilo" o "Microsoft Word para Windows".</span><span class="sxs-lookup"><span data-stu-id="90e02-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="90e02-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="90e02-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-136">El miembro de **valor** identifica la versión de este archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="90e02-137">Por ejemplo, el **valor** puede ser "3,00 a" o "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="90e02-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="90e02-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span><span class="sxs-lookup"><span data-stu-id="90e02-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-139">El miembro de **valor** identifica el nombre interno del archivo, si existe alguno.</span><span class="sxs-lookup"><span data-stu-id="90e02-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="90e02-140">Por ejemplo, esta cadena podría contener el nombre del módulo para un archivo DLL, un nombre de dispositivo virtual para un dispositivo virtual de Windows o un nombre de dispositivo para un controlador de dispositivo de MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="90e02-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="90e02-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="90e02-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-142">El miembro de **valor** describe todos los avisos de propiedad intelectual, marcas comerciales y marcas registradas que se aplican al archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="90e02-143">Esto debe incluir el texto completo de todos los avisos, símbolos legales, fechas de copyright, números de marcas comerciales, etc.</span><span class="sxs-lookup"><span data-stu-id="90e02-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="90e02-144">En inglés, esta cadena debe tener el formato "Copyright Microsoft Corp. 1990 1994".</span><span class="sxs-lookup"><span data-stu-id="90e02-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="90e02-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="90e02-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-146">El miembro **Value** describe todas las marcas comerciales y marcas registradas que se aplican al archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="90e02-147">Esto debe incluir el texto completo de todos los avisos, símbolos legales, números de marcas comerciales, etc.</span><span class="sxs-lookup"><span data-stu-id="90e02-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="90e02-148">En inglés, esta cadena debe tener el formato "Windows es una marca comercial de Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="90e02-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="90e02-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="90e02-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-150">El miembro de **valor** identifica el nombre original del archivo, sin incluir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="90e02-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="90e02-151">Esto permite que una aplicación determine si un usuario ha cambiado el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="90e02-152">Este nombre no puede ser MS-DOS 8,3-Format si el archivo es específico de un sistema de archivos que no es FAT.</span><span class="sxs-lookup"><span data-stu-id="90e02-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="90e02-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="90e02-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-154">El miembro de **valor** describe quién, dónde y por qué se compiló esta versión privada del archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="90e02-155">Esta cadena solo debe estar presente si la marca **vs \_ FF \_ PRIVATEBUILD** se establece en el miembro **dwFileFlags** de la estructura [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="90e02-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="90e02-156">Por ejemplo, el **valor** podría ser "compilado por Oscar en \\ OSCAR2".</span><span class="sxs-lookup"><span data-stu-id="90e02-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="90e02-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**NombreDeProducto**</span><span class="sxs-lookup"><span data-stu-id="90e02-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-158">El miembro de **valor** identifica el nombre del producto con el que se distribuye este archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="90e02-159">Por ejemplo, esta cadena podría ser "Microsoft Windows".</span><span class="sxs-lookup"><span data-stu-id="90e02-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="90e02-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="90e02-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-161">El miembro de **valor** identifica la versión del producto con el que se distribuye este archivo.</span><span class="sxs-lookup"><span data-stu-id="90e02-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="90e02-162">Por ejemplo, el **valor** puede ser "3,00 a" o "5,00. RC2".</span><span class="sxs-lookup"><span data-stu-id="90e02-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="90e02-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="90e02-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="90e02-164">El miembro **Value** describe el modo en que esta versión del archivo difiere de la versión normal.</span><span class="sxs-lookup"><span data-stu-id="90e02-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="90e02-165">Esta entrada solo debe estar presente si la marca **vs \_ FF \_ SPECIALBUILD** se establece en el miembro **dwFileFlags** de la estructura [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="90e02-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="90e02-166">Por ejemplo, el **valor** podría ser "compilación privada para la solución de problemas del mouse en los equipos M250 y M250E".</span><span class="sxs-lookup"><span data-stu-id="90e02-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="90e02-167">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="90e02-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="90e02-168">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="90e02-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90e02-169">Tantas palabras como sea necesario para alinear el miembro de **valor** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="90e02-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="90e02-170">**Valor**</span><span class="sxs-lookup"><span data-stu-id="90e02-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="90e02-171">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="90e02-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90e02-172">Cadena terminada en cero.</span><span class="sxs-lookup"><span data-stu-id="90e02-172">A zero-terminated string.</span></span> <span data-ttu-id="90e02-173">Vea la descripción del miembro **szKey** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="90e02-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90e02-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90e02-174">Remarks</span></span>

<span data-ttu-id="90e02-175">Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="90e02-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="90e02-176">Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="90e02-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="90e02-177">Una estructura de **cadena** puede tener un valor **szKey** de, por ejemplo, "CompanyName" y un **valor** de "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="90e02-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="90e02-178">Otra estructura de **cadena** con el mismo valor de **szKey** podría contener un **valor** de "Microsoft GmbH".</span><span class="sxs-lookup"><span data-stu-id="90e02-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="90e02-179">Esto puede ocurrir si la segunda estructura de **cadena** estaba asociada a una estructura [**StringTable**](stringtable.md) cuyo valor de **szKey** es 040704b0, alemán o Unicode.</span><span class="sxs-lookup"><span data-stu-id="90e02-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e02-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90e02-180">Requirements</span></span>



| <span data-ttu-id="90e02-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="90e02-181">Requirement</span></span> | <span data-ttu-id="90e02-182">Value</span><span class="sxs-lookup"><span data-stu-id="90e02-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90e02-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90e02-183">Minimum supported client</span></span><br/> | <span data-ttu-id="90e02-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90e02-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90e02-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90e02-185">Minimum supported server</span></span><br/> | <span data-ttu-id="90e02-186">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90e02-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="90e02-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="90e02-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="90e02-188">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="90e02-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90e02-189">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="90e02-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="90e02-190">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="90e02-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="90e02-191">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="90e02-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="90e02-192">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="90e02-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="90e02-193">**Vista**</span><span class="sxs-lookup"><span data-stu-id="90e02-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90e02-194">Información de versión</span><span class="sxs-lookup"><span data-stu-id="90e02-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





