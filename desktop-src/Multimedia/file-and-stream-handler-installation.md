---
title: Instalación del controlador de archivos y secuencias
description: Instalación del controlador de archivos y secuencias
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779134"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="f705b-103">Instalación del controlador de archivos y secuencias</span><span class="sxs-lookup"><span data-stu-id="f705b-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="f705b-104">La biblioteca AVIFile usa controladores de archivos y secuencias instalados para leer y escribir archivos AVI y secuencias.</span><span class="sxs-lookup"><span data-stu-id="f705b-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="f705b-105">Un controlador se instala cuando reside en el directorio del sistema de Windows y el registro contiene la siguiente información necesaria para describir e identificar un controlador:</span><span class="sxs-lookup"><span data-stu-id="f705b-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="f705b-106">Identificador de clase de 16 bytes para el controlador</span><span class="sxs-lookup"><span data-stu-id="f705b-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="f705b-107">Breve descripción del controlador</span><span class="sxs-lookup"><span data-stu-id="f705b-107">A brief description of the handler</span></span>
-   <span data-ttu-id="f705b-108">Nombre del archivo que contiene el controlador.</span><span class="sxs-lookup"><span data-stu-id="f705b-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="f705b-109">La extensión de archivo que un controlador de archivos puede procesar.</span><span class="sxs-lookup"><span data-stu-id="f705b-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="f705b-110">Acceso a archivos y otras propiedades asociadas a un controlador de archivos</span><span class="sxs-lookup"><span data-stu-id="f705b-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="f705b-111">Códigos de cuatro caracteres que identifican los tipos de secuencia que un controlador de flujo puede procesar</span><span class="sxs-lookup"><span data-stu-id="f705b-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="f705b-112">La biblioteca AVIFile consulta al registro los controladores que son externos a una aplicación al abrir archivos y obtener acceso a secuencias.</span><span class="sxs-lookup"><span data-stu-id="f705b-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="f705b-113">El resultado de una consulta correcta devuelve el nombre de archivo de un controlador que puede procesar el tipo de archivo o de secuencia especificado en la consulta.</span><span class="sxs-lookup"><span data-stu-id="f705b-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="f705b-114">El registro muestra cada controlador mediante la creación de tres entradas que tienen el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="f705b-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="f705b-115">Estas entradas se componen de las siguientes partes.</span><span class="sxs-lookup"><span data-stu-id="f705b-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="f705b-116">Parte</span><span class="sxs-lookup"><span data-stu-id="f705b-116">Part</span></span>                                   | <span data-ttu-id="f705b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f705b-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f705b-118">\_clase HKEY \_ raíz</span><span class="sxs-lookup"><span data-stu-id="f705b-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="f705b-119">Identifica la entrada raíz del registro.</span><span class="sxs-lookup"><span data-stu-id="f705b-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="f705b-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="f705b-120">Clsid</span></span>                                  | <span data-ttu-id="f705b-121">Identifica esta entrada como un identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="f705b-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="f705b-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="f705b-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="f705b-123">Especifica un identificador de interfaz (IID) o un identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="f705b-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="f705b-124">Este valor es un identificador único de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="f705b-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="f705b-125">(También se puede hacer referencia al identificador como un GUID o un UUID en otros manuales).</span><span class="sxs-lookup"><span data-stu-id="f705b-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="f705b-126">Lector/escritor de archivos de onda</span><span class="sxs-lookup"><span data-stu-id="f705b-126">Wave File reader/writer</span></span>                | <span data-ttu-id="f705b-127">Especifica una cadena para describir el controlador.</span><span class="sxs-lookup"><span data-stu-id="f705b-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="f705b-128">Esta cadena se puede mostrar en cuadros de diálogo para seleccionar secuencias y controladores de archivos.</span><span class="sxs-lookup"><span data-stu-id="f705b-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="f705b-129">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="f705b-129">InProcServer32</span></span>                         | <span data-ttu-id="f705b-130">Especifica el archivo (en este ejemplo, WAVEFILE.DLL) que se puede cargar para controlar esta clase.</span><span class="sxs-lookup"><span data-stu-id="f705b-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="f705b-131">AVIFile</span><span class="sxs-lookup"><span data-stu-id="f705b-131">AVIFile</span></span>                                | <span data-ttu-id="f705b-132">Especifica las propiedades de un controlador de archivos.</span><span class="sxs-lookup"><span data-stu-id="f705b-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="f705b-133">En este ejemplo, el controlador puede leer y escribir en un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="f705b-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="f705b-134">Un controlador de archivos puede tener una o varias de sus propiedades almacenadas en el registro.</span><span class="sxs-lookup"><span data-stu-id="f705b-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="f705b-135">Las constantes siguientes identifican las propiedades asociadas actualmente a un archivo.</span><span class="sxs-lookup"><span data-stu-id="f705b-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="f705b-136">Constante</span><span class="sxs-lookup"><span data-stu-id="f705b-136">Constant</span></span>                        | <span data-ttu-id="f705b-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="f705b-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="f705b-138">AVIFILEHANDLER \_ CANACCEPTNONRGB</span><span class="sxs-lookup"><span data-stu-id="f705b-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="f705b-139">Indica que un controlador de archivos puede procesar datos de imagen distintos de RGB.</span><span class="sxs-lookup"><span data-stu-id="f705b-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="f705b-140">AVIFILEHANDLER \_ CANREAD</span><span class="sxs-lookup"><span data-stu-id="f705b-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="f705b-141">Indica que un controlador de archivos puede abrir un archivo con acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="f705b-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="f705b-142">AVIFILEHANDLER \_ CANWRITE</span><span class="sxs-lookup"><span data-stu-id="f705b-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="f705b-143">Indica que un controlador de archivos puede abrir un archivo con acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="f705b-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="f705b-144">Al crear un archivo o un controlador de secuencias, puede obtener un nuevo identificador ejecutando UUIDGEN.EXE.</span><span class="sxs-lookup"><span data-stu-id="f705b-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="f705b-145">Utilice siempre UUIDGEN.EXE para crear un nuevo identificador.</span><span class="sxs-lookup"><span data-stu-id="f705b-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="f705b-146">El número hexadecimal de 16 bytes creado por este archivo ejecutable identificará de forma única el controlador.</span><span class="sxs-lookup"><span data-stu-id="f705b-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="f705b-147">La biblioteca AVIFile usa entradas adicionales en el registro para identificar un identificador de clase basado en la extensión de archivo que un controlador de archivos puede procesar o un código de cuatro caracteres que un controlador de archivo o secuencia puede procesar.</span><span class="sxs-lookup"><span data-stu-id="f705b-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="f705b-148">Por ejemplo, las siguientes entradas asocian un identificador de clase a la extensión de archivo. WAV y el código de cuatro caracteres "WAVE":</span><span class="sxs-lookup"><span data-stu-id="f705b-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="f705b-149">Estas entradas se componen de las siguientes partes.</span><span class="sxs-lookup"><span data-stu-id="f705b-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="f705b-150">Parte</span><span class="sxs-lookup"><span data-stu-id="f705b-150">Part</span></span>                                   | <span data-ttu-id="f705b-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="f705b-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f705b-152">\_clase HKEY \_ raíz</span><span class="sxs-lookup"><span data-stu-id="f705b-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="f705b-153">Identifica la entrada raíz del registro.</span><span class="sxs-lookup"><span data-stu-id="f705b-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="f705b-154">AVIFile</span><span class="sxs-lookup"><span data-stu-id="f705b-154">AVIFile</span></span>                                | <span data-ttu-id="f705b-155">Identifica esta entrada como una entrada utilizada por AVIFile.</span><span class="sxs-lookup"><span data-stu-id="f705b-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="f705b-156">Extensiones</span><span class="sxs-lookup"><span data-stu-id="f705b-156">Extensions</span></span>                             | <span data-ttu-id="f705b-157">Especifica la extensión de archivo (en este ejemplo,. WAV) que un controlador de archivos puede procesar.</span><span class="sxs-lookup"><span data-stu-id="f705b-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="f705b-158">RIFFHandlers</span><span class="sxs-lookup"><span data-stu-id="f705b-158">RIFFHandlers</span></span>                           | <span data-ttu-id="f705b-159">Especifica el código de cuatro caracteres (en este ejemplo, "WAVE") que un controlador de archivo o secuencia puede procesar.</span><span class="sxs-lookup"><span data-stu-id="f705b-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="f705b-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="f705b-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="f705b-161">Especifica un identificador de interfaz (IID) o un identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="f705b-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="f705b-162">Si distribuye la secuencia o el controlador de archivo sin una aplicación de instalación para instalarlo en el sistema del usuario, debe incluir un. Archivo REG para que el usuario pueda instalar el controlador.</span><span class="sxs-lookup"><span data-stu-id="f705b-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="f705b-163">El usuario utilizará el editor del registro para crear entradas del registro para el flujo o el controlador de archivos.</span><span class="sxs-lookup"><span data-stu-id="f705b-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="f705b-164">En el ejemplo siguiente se muestra el contenido de un típico. Archivo REG.</span><span class="sxs-lookup"><span data-stu-id="f705b-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="f705b-165">La primera entrada del ejemplo siguiente es la cadena descriptiva del controlador.</span><span class="sxs-lookup"><span data-stu-id="f705b-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="f705b-166">La segunda entrada identifica el archivo que contiene el controlador.</span><span class="sxs-lookup"><span data-stu-id="f705b-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="f705b-167">La tercera entrada identifica las propiedades del controlador de archivos (en este caso, acceso de solo lectura a los archivos).</span><span class="sxs-lookup"><span data-stu-id="f705b-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="f705b-168">La cuarta entrada asocia el tipo de archivo que procesa el controlador (en este caso, los archivos con. Extensión de nombre de archivo JPG) con el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="f705b-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="f705b-169">Al crear este archivo, guárdelo con un. REG extensión para identificarla como un archivo de actualización para el registro.</span><span class="sxs-lookup"><span data-stu-id="f705b-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="f705b-170">Además, sustituya un IID único para el código de 16 bytes que se usa en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f705b-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 




