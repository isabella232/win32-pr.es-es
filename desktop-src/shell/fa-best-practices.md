---
description: La siguiente lista son prácticas recomendadas que debe usar al trabajar con asociaciones de archivo.
title: Prácticas recomendadas para asociaciones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541086"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="56da0-103">Prácticas recomendadas para asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-103">Best Practices for File Associations</span></span>

<span data-ttu-id="56da0-104">La siguiente lista son prácticas recomendadas que debe usar al trabajar con asociaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="56da0-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="56da0-105">No copiar asociaciones de archivo del registro</span><span class="sxs-lookup"><span data-stu-id="56da0-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="56da0-106">Evite Hard-Coding rutas de acceso en el registro siempre que sea posible</span><span class="sxs-lookup"><span data-stu-id="56da0-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="56da0-107">Ajustar siempre las cadenas de expansión entre comillas</span><span class="sxs-lookup"><span data-stu-id="56da0-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="56da0-108">No confunda reproducción automática/Autorun con asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="56da0-109">No confunda la base de datos MIME de Internet Explorer con asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="56da0-110">Usar ProgID con formato y con control de versiones correctos</span><span class="sxs-lookup"><span data-stu-id="56da0-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="56da0-111">No usar extensiones de nombre de archivo cortas</span><span class="sxs-lookup"><span data-stu-id="56da0-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="56da0-112">Registrar nuevos tipos de archivo en la base de datos MIME de IANA</span><span class="sxs-lookup"><span data-stu-id="56da0-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="56da0-113">Registrarse con el servicio Web de Windows para asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="56da0-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56da0-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="56da0-115">No copiar asociaciones de archivo del registro</span><span class="sxs-lookup"><span data-stu-id="56da0-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="56da0-116">Se recomienda no copiar las asociaciones de archivo existentes del registro.</span><span class="sxs-lookup"><span data-stu-id="56da0-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="56da0-117">A menudo, esto conduce a la propagación de asociaciones de archivo con un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="56da0-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="56da0-118">En su lugar, debe seguir los pasos descritos en el [escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="56da0-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="56da0-119">Evite Hard-Coding rutas de acceso en el registro siempre que sea posible</span><span class="sxs-lookup"><span data-stu-id="56da0-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="56da0-120">Del mismo modo que las rutas de acceso de código duro en los programas pueden causar problemas, las rutas de acceso de código duro en el registro también pueden provocar problemas.</span><span class="sxs-lookup"><span data-stu-id="56da0-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="56da0-121">En su lugar, debe usar las cadenas de expansión del registro (REG \_ Expand \_ SZ) para proporcionar independencia de la ruta de acceso cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="56da0-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="56da0-122">Por ejemplo, en lugar de usar este método:</span><span class="sxs-lookup"><span data-stu-id="56da0-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="56da0-123">Debe usar este método:</span><span class="sxs-lookup"><span data-stu-id="56da0-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="56da0-124">Ajustar siempre las cadenas de expansión entre comillas</span><span class="sxs-lookup"><span data-stu-id="56da0-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="56da0-125">Expandir cadenas puede contener espacios cuando se expanden.</span><span class="sxs-lookup"><span data-stu-id="56da0-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="56da0-126">Dado que los espacios suelen interpretarse como delimitadores de argumentos, causan problemas en determinadas circunstancias.</span><span class="sxs-lookup"><span data-stu-id="56da0-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="56da0-127">Por ejemplo, un comando para invocar mi programa puede almacenarse en el registro como:</span><span class="sxs-lookup"><span data-stu-id="56da0-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="56da0-128">Mi programa espera que %1 sea la ruta de acceso completa a un nombre de archivo y %2 es un modificador para indicar alguna acción.</span><span class="sxs-lookup"><span data-stu-id="56da0-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="56da0-129">Si este comando se ejecuta con **los argumentos C: \\ archivos de programa \\ Mis documentos \\document.txt** y **/Print**, y suponiendo que la raíz de c: \\ WinNT, se expande a:</span><span class="sxs-lookup"><span data-stu-id="56da0-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="56da0-130">En este caso, el programa interpreta que el primer argumento es C: \\ Program y el segundo argumento es files \\ My, que no es el comportamiento previsto.</span><span class="sxs-lookup"><span data-stu-id="56da0-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="56da0-131">Los argumentos se interpretan correctamente, sin embargo, independientemente de si contienen espacios, si las cadenas de expansión se incluyen entre comillas de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="56da0-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="56da0-132">No confunda reproducción automática/Autorun con asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="56da0-133">Las asociaciones de archivos son similares a la reproducción automática y la ejecución automática de algunas maneras.</span><span class="sxs-lookup"><span data-stu-id="56da0-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="56da0-134">Sin embargo, la reproducción automática y la ejecución automática ofrecen instalaciones independientes y distintas de las proporcionadas por las asociaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="56da0-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="56da0-135">Para obtener más información [, consulte crear una aplicación de CD-ROM habilitada para Autorun](autoplay.md).</span><span class="sxs-lookup"><span data-stu-id="56da0-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="56da0-136">No confunda la base de datos MIME de Internet Explorer con asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="56da0-137">Las asociaciones de archivos son similares a la base de datos MIME de Windows Internet Explorer, en los tipos de archivo que pueden (y deberían) incluir una definición de tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="56da0-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="56da0-138">Sin embargo, la base de datos MIME de Internet Explorer es independiente y distinta de las asociaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="56da0-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="56da0-139">Usar ProgID con formato y con control de versiones correctos</span><span class="sxs-lookup"><span data-stu-id="56da0-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="56da0-140">Utilice siempre los [ProgID con versión](fa-progids.md), incluso si solo hay una versión de ProgID.</span><span class="sxs-lookup"><span data-stu-id="56da0-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="56da0-141">Los ProgID con versión ayudan a evitar conflictos de ProgID y sobrescrituras.</span><span class="sxs-lookup"><span data-stu-id="56da0-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="56da0-142">También permiten que las distintas versiones de una aplicación coexistan.</span><span class="sxs-lookup"><span data-stu-id="56da0-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="56da0-143">No usar extensiones de nombre de archivo cortas</span><span class="sxs-lookup"><span data-stu-id="56da0-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="56da0-144">Las extensiones de nombre de archivo largas ofrecen las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="56da0-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="56da0-145">La longitud limitada de las extensiones cortas hace que sean propensos a *colisiones de extensión.*</span><span class="sxs-lookup"><span data-stu-id="56da0-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="56da0-146">Se produce una colisión de extensión cuando se utiliza la misma extensión para clasificar varios tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="56da0-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="56da0-147">El uso de extensiones largas reduce considerablemente las posibilidades de una colisión.</span><span class="sxs-lookup"><span data-stu-id="56da0-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="56da0-148">Los nombres de archivo cortos tienden a ser algo crípticos.</span><span class="sxs-lookup"><span data-stu-id="56da0-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="56da0-149">Las extensiones largas suelen ser más significativas, ya que se puede insertar información adicional en la extensión.</span><span class="sxs-lookup"><span data-stu-id="56da0-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="56da0-150">Para obtener más información, vea [extensiones de nombre de archivo](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="56da0-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="56da0-151">Registrar nuevos tipos de archivo en la base de datos MIME de IANA</span><span class="sxs-lookup"><span data-stu-id="56da0-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="56da0-152">La autoridad de asignación de números de Internet (IANA) mantiene una base de datos pública de tipos MIME registrados.</span><span class="sxs-lookup"><span data-stu-id="56da0-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="56da0-153">Al definir un nuevo tipo de archivo público, se recomienda definir también un tipo MIME para el tipo de archivo y registrar este tipo con la IANA.</span><span class="sxs-lookup"><span data-stu-id="56da0-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="56da0-154">El registro no tiene ningún costo.</span><span class="sxs-lookup"><span data-stu-id="56da0-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="56da0-155">Registrarse con el servicio Web de Windows para asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="56da0-156">Los desarrolladores de aplicaciones pueden registrarse con el servicio Web de Windows que usan los usuarios para buscar aplicaciones que puedan funcionar en tipos de archivo específicos.</span><span class="sxs-lookup"><span data-stu-id="56da0-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="56da0-157">El proceso de registro con el servicio Web se detalla en el [proceso de incorporación del sistema de Asociación de archivos de Windows](https://support.microsoft.com/kb/929149).</span><span class="sxs-lookup"><span data-stu-id="56da0-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56da0-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56da0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56da0-159">Escenario de ejemplo de Asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="56da0-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="56da0-160">Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="56da0-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="56da0-161">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="56da0-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="56da0-162">Establecer los valores predeterminados de acceso a programas y del equipo (SPAD)</span><span class="sxs-lookup"><span data-stu-id="56da0-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 



