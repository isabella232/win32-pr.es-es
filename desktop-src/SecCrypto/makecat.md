---
description: Herramienta CryptoAPI que crea un archivo de catálogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908087"
---
# <a name="makecat"></a><span data-ttu-id="27a8e-103">MakeCat</span><span class="sxs-lookup"><span data-stu-id="27a8e-103">MakeCat</span></span>

<span data-ttu-id="27a8e-104">La herramienta MakeCat es una herramienta CryptoAPI que crea un archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="27a8e-105">MakeCat está disponible como parte del kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0 y está instalado, de forma predeterminada, en la \\ carpeta bin de la ruta de instalación de SDK.</span><span class="sxs-lookup"><span data-stu-id="27a8e-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="27a8e-106">La herramienta MakeCat usa la siguiente sintaxis de comando:</span><span class="sxs-lookup"><span data-stu-id="27a8e-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="27a8e-107">**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="27a8e-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="27a8e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27a8e-108">Parameters</span></span>



| <span data-ttu-id="27a8e-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="27a8e-109">Parameter</span></span>             | <span data-ttu-id="27a8e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a8e-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a8e-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="27a8e-111">**-n**</span></span><br/>     | <span data-ttu-id="27a8e-112">No se detiene en un error recuperable.</span><span class="sxs-lookup"><span data-stu-id="27a8e-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="27a8e-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="27a8e-113">**-r**</span></span><br/>     | <span data-ttu-id="27a8e-114">Fuerza a MakeCat a finalizar si encuentra errores recuperables.</span><span class="sxs-lookup"><span data-stu-id="27a8e-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="27a8e-115">En concreto, terminará al procesar las entradas de la sección de archivos de catálogo de un archivo. CDF.</span><span class="sxs-lookup"><span data-stu-id="27a8e-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="27a8e-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="27a8e-116">**-v**</span></span><br/>     | <span data-ttu-id="27a8e-117">Detallado.</span><span class="sxs-lookup"><span data-stu-id="27a8e-117">Verbose.</span></span> <span data-ttu-id="27a8e-118">Muestra todos los mensajes de progreso y de error.</span><span class="sxs-lookup"><span data-stu-id="27a8e-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="27a8e-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="27a8e-119">*FileName*</span></span><br/> | <span data-ttu-id="27a8e-120">Nombre del archivo. CDF que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="27a8e-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="27a8e-121">Para obtener la estructura y el contenido necesarios, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="27a8e-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="27a8e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27a8e-122">Remarks</span></span>

<span data-ttu-id="27a8e-123">El archivo. CDF debe compilarse con las siguientes especificaciones.</span><span class="sxs-lookup"><span data-stu-id="27a8e-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="27a8e-124">La última entrada del archivo. CDF siempre debe tener un carácter de nueva línea explícito al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="27a8e-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="27a8e-125">La \[ \] sección CatalogHeader define información sobre todo el archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="27a8e-126">Opción</span><span class="sxs-lookup"><span data-stu-id="27a8e-126">Option</span></span>                    | <span data-ttu-id="27a8e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a8e-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a8e-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="27a8e-128">Name</span></span><br/>           | <span data-ttu-id="27a8e-129">Nombre del archivo de catálogo, incluida su extensión.</span><span class="sxs-lookup"><span data-stu-id="27a8e-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="27a8e-130">ResultDir</span><span class="sxs-lookup"><span data-stu-id="27a8e-130">ResultDir</span></span><br/>      | <span data-ttu-id="27a8e-131">Directorio donde se colocará el archivo. cat creado.</span><span class="sxs-lookup"><span data-stu-id="27a8e-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="27a8e-132">Si no se indica, se usa el directorio actual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27a8e-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="27a8e-133">Si el directorio no existe, se crea.</span><span class="sxs-lookup"><span data-stu-id="27a8e-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="27a8e-134">PublicVersion</span><span class="sxs-lookup"><span data-stu-id="27a8e-134">PublicVersion</span></span><br/>  | <span data-ttu-id="27a8e-135">Esta opción no se admite.</span><span class="sxs-lookup"><span data-stu-id="27a8e-135">This option is not supported.</span></span> <br/> <span data-ttu-id="27a8e-136">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Versión del catálogo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="27a8e-137">Si se deja en blanco, se usa el valor predeterminado, 1.</span><span class="sxs-lookup"><span data-stu-id="27a8e-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="27a8e-138">CatalogVersion</span><span class="sxs-lookup"><span data-stu-id="27a8e-138">CatalogVersion</span></span><br/> | <span data-ttu-id="27a8e-139">Versión del catálogo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-139">Catalog version.</span></span> <span data-ttu-id="27a8e-140">Si la versión no está presente o se establece en 1, "0x100" se pasa al parámetro *dwPublicVersion* de la función [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) y se crea un archivo de catálogo de la versión 1.</span><span class="sxs-lookup"><span data-stu-id="27a8e-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="27a8e-141">La opción HashAlgorithms debe estar vacía o contener SHA1.</span><span class="sxs-lookup"><span data-stu-id="27a8e-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="27a8e-142">Si la versión se establece en 2, se pasa "0x200" al parámetro *dwPublicVersion* de la función [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) y se crea un archivo de catálogo de la versión 2.</span><span class="sxs-lookup"><span data-stu-id="27a8e-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="27a8e-143">La opción HashAlgorithms debe contener SHA256.</span><span class="sxs-lookup"><span data-stu-id="27a8e-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="27a8e-144">Si esta opción está presente pero contiene cualquier valor distinto de 1 o 2, se producirá un error en la herramienta MakeCat.</span><span class="sxs-lookup"><span data-stu-id="27a8e-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="27a8e-145">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta opción no se admite.</span><span class="sxs-lookup"><span data-stu-id="27a8e-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="27a8e-146">HashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="27a8e-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="27a8e-147">Nombre del algoritmo hash usado.</span><span class="sxs-lookup"><span data-stu-id="27a8e-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="27a8e-148">Para obtener más información, vea la opción CatalogVersion.</span><span class="sxs-lookup"><span data-stu-id="27a8e-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="27a8e-149">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta opción no se admite.</span><span class="sxs-lookup"><span data-stu-id="27a8e-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="27a8e-150">PageHashes</span><span class="sxs-lookup"><span data-stu-id="27a8e-150">PageHashes</span></span><br/>     | <span data-ttu-id="27a8e-151">Especifica si se van a aplicar algoritmos hash a los archivos enumerados en la <HASH> opción de la \[ \] sección CatalogFiles</span><span class="sxs-lookup"><span data-stu-id="27a8e-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="27a8e-152">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta opción no se admite.</span><span class="sxs-lookup"><span data-stu-id="27a8e-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="27a8e-153">EncodingType</span><span class="sxs-lookup"><span data-stu-id="27a8e-153">EncodingType</span></span><br/>   | <span data-ttu-id="27a8e-154">Tipo de codificación de mensajes usada.</span><span class="sxs-lookup"><span data-stu-id="27a8e-154">Type of message encoding used.</span></span> <span data-ttu-id="27a8e-155">Si se deja en blanco, el valor predeterminado de EncodingType es PKCS 7 codificación ASN de codificación de ASN \_ \_ \_ \| \_ \_ , 0x00010001.</span><span class="sxs-lookup"><span data-stu-id="27a8e-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="27a8e-156">\[En la \] sección CatalogFiles se define cada miembro del archivo de catálogo con archivos de varios tipos y atributos de varios tipos en grupos independientes.</span><span class="sxs-lookup"><span data-stu-id="27a8e-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27a8e-157">Opción</span><span class="sxs-lookup"><span data-stu-id="27a8e-157">Option</span></span></th>
<th><span data-ttu-id="27a8e-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a8e-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27a8e-159">etiqueta de referencia</span><span class="sxs-lookup"><span data-stu-id="27a8e-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="27a8e-160">Referencia de texto al archivo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-160">Text reference to the file.</span></span> <span data-ttu-id="27a8e-161">Puede incluir cualquier carácter de texto ASCII excepto el signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="27a8e-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="27a8e-162">El sistema debe poder reproducir esta etiqueta después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="27a8e-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="27a8e-163">Use <HASH> como prefijo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="27a8e-164">Esto da como resultado que la etiqueta sea el hash del archivo en forma de cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="27a8e-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27a8e-165">Ruta de acceso y nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="27a8e-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="27a8e-166">El nombre de archivo, incluida la extensión que se va a analizar y la ruta de acceso relativa al archivo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="27a8e-167">Cualquier tipo de archivo que se pueda firmar con SignTool puede agregarse a un catálogo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="27a8e-168">Por ejemplo, los nombres de archivo con las siguientes extensiones, entre otros, se pueden agregar a un catálogo:. exe,. cab,. cat,. ocx,. dll y. STL.</span><span class="sxs-lookup"><span data-stu-id="27a8e-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27a8e-169">ALTSIPID</span><span class="sxs-lookup"><span data-stu-id="27a8e-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="27a8e-170">GUID de SIP que se va a utilizar para el hash en lugar del SIP estándar basado en el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="27a8e-171">Esta entrada es opcional.</span><span class="sxs-lookup"><span data-stu-id="27a8e-171">This entry is optional.</span></span> <span data-ttu-id="27a8e-172">Si se omite esta entrada, se aplicará un algoritmo hash al miembro mediante el SIP predeterminado.</span><span class="sxs-lookup"><span data-stu-id="27a8e-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="27a8e-173">Si no se encuentra ningún SIP instalado de forma predeterminada, se usará el SIP plano.</span><span class="sxs-lookup"><span data-stu-id="27a8e-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27a8e-174">guid</span><span class="sxs-lookup"><span data-stu-id="27a8e-174">guid</span></span><br/></td>
<td><span data-ttu-id="27a8e-175">Representación de texto de un GUID.</span><span class="sxs-lookup"><span data-stu-id="27a8e-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27a8e-176">ATTRx</span><span class="sxs-lookup"><span data-stu-id="27a8e-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="27a8e-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27a8e-177">Optional.</span></span> <span data-ttu-id="27a8e-178">Atributo o instrucción sobre el archivo o el contenido.</span><span class="sxs-lookup"><span data-stu-id="27a8e-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="27a8e-179">Puede haber cualquier número de atributos, incluido ninguno.</span><span class="sxs-lookup"><span data-stu-id="27a8e-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27a8e-180">type</span><span class="sxs-lookup"><span data-stu-id="27a8e-180">type</span></span><br/></td>
<td><span data-ttu-id="27a8e-181">Define el tipo de atributo que se va a agregar en el formato 0x00000000 (texto).</span><span class="sxs-lookup"><span data-stu-id="27a8e-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="27a8e-182">Esta opción puede ser<strong>una combinación OR bit a bit</strong> de cero o más de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="27a8e-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="27a8e-183">atributo autenticado de 0x10000000 (firmado, incluido en el hash).</span><span class="sxs-lookup"><span data-stu-id="27a8e-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="27a8e-184">0x20000000 atributo no autenticado (sin signo, no incluido en el hash, no comprobable).</span><span class="sxs-lookup"><span data-stu-id="27a8e-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="27a8e-185">el atributo 0x01000000 no se replicará en las entradas SHA1 de un catálogo CatalogVersion 2.</span><span class="sxs-lookup"><span data-stu-id="27a8e-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="27a8e-186">el atributo 0x00010000 se representa en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="27a8e-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="27a8e-187">No se realizará ninguna conversión.</span><span class="sxs-lookup"><span data-stu-id="27a8e-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="27a8e-188">el atributo 0x00020000 se representa en la codificación de base 64.</span><span class="sxs-lookup"><span data-stu-id="27a8e-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="27a8e-189">Se utiliza para representar datos binarios.</span><span class="sxs-lookup"><span data-stu-id="27a8e-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="27a8e-190">0x00000001 Attribute es un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="27a8e-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="27a8e-191">Use la opción OID como nombre.</span><span class="sxs-lookup"><span data-stu-id="27a8e-191">Use the oid option for the name.</span></span> <span data-ttu-id="27a8e-192">Este atributo es lento; por lo tanto, use esta opción con moderación.</span><span class="sxs-lookup"><span data-stu-id="27a8e-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="27a8e-193">un <a href="/windows/desktop/SecGloss/o-gly"><em>identificador de objeto</em></a> (OID) hace referencia a un atributo 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="27a8e-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27a8e-194">oid</span><span class="sxs-lookup"><span data-stu-id="27a8e-194">oid</span></span><br/></td>
<td><span data-ttu-id="27a8e-195">Representación de texto de la clave de referencia del atributo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="27a8e-196">Es un OID en forma de cadena de texto en notación cuádruple con puntos (por ejemplo, a.b.c. d) o un nombre de texto.</span><span class="sxs-lookup"><span data-stu-id="27a8e-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27a8e-197">value</span><span class="sxs-lookup"><span data-stu-id="27a8e-197">value</span></span><br/></td>
<td><span data-ttu-id="27a8e-198">Representación de texto del valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="27a8e-199">El tipo de representación de texto utilizado depende del valor de la opción Type.</span><span class="sxs-lookup"><span data-stu-id="27a8e-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="27a8e-200">Los caracteres EOL determinan la longitud.</span><span class="sxs-lookup"><span data-stu-id="27a8e-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="27a8e-201">Aplica un algoritmo hash al archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="27a8e-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="27a8e-202">El archivo de catálogo generado no tiene signo.</span><span class="sxs-lookup"><span data-stu-id="27a8e-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="27a8e-203">Si se va a firmar antes de transmitir, se firma con [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="27a8e-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
