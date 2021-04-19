---
description: En el ejemplo siguiente, una empresa hipotética de desarrollo de software llamada Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Ejemplo de asociación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b92922bb907c4dd90b3e2bdc3d16c8e8b52e6a
ms.sourcegitcommit: b0d03febac36ff77cba034615b94ea103311398d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/19/2021
ms.locfileid: "107715793"
---
# <a name="file-association-example"></a><span data-ttu-id="63c59-103">Ejemplo de asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="63c59-103">File Association Example</span></span>

<span data-ttu-id="63c59-104">En el ejemplo siguiente, una compañía hipotética de desarrollo de software llamada Litware, Inc. crea un nuevo reproductor de audio llamado LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="63c59-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="63c59-105">Litware quiere diseñar una asociación de archivos entre LitwarePlayer y su tipo de archivo principal, que usa un formato de audio recién desarrollado que permite almacenar un CD de audio completo en menos de 10 kilobytes de memoria sin pérdida de calidad.</span><span class="sxs-lookup"><span data-stu-id="63c59-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63c59-106">Este tema no se aplica a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63c59-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="63c59-107">La forma en que funcionan las asociaciones de archivos predeterminadas ha cambiado Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63c59-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="63c59-108">Para obtener más información, vea la sección Sobre los cambios en Windows 10 **controla las aplicaciones predeterminadas** en [esta entrada](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="63c59-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="63c59-109">Diseñar una nueva asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="63c59-109">Designing a New File Association</span></span>

<span data-ttu-id="63c59-110">La empresa debe realizar los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="63c59-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="63c59-111">**Decida si el nuevo tipo de archivo debe tratarse como público o privado.**</span><span class="sxs-lookup"><span data-stu-id="63c59-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="63c59-112">Este nuevo tipo de archivo es un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="63c59-112">This new file type is a media type.</span></span> <span data-ttu-id="63c59-113">Dado que los usuarios intercambian archivos multimedia entre varias plataformas y puede [](fa-file-types.md) haber otras aplicaciones que necesiten leer el formato LitwarePlayer, un tipo de archivo público es el más adecuado.</span><span class="sxs-lookup"><span data-stu-id="63c59-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="63c59-114">**Determine si este tipo de archivo ya está definido.**</span><span class="sxs-lookup"><span data-stu-id="63c59-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="63c59-115">Compruebe la base de datos MIME de Internet Assigned Numbers Authority (IANA) y otras bases de datos de tipo de archivo público en Internet para determinar que no se ha definido ningún tipo de archivo comparable.</span><span class="sxs-lookup"><span data-stu-id="63c59-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="63c59-116">Dado que se trata de un nuevo formato de archivo, debe definir un nuevo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="63c59-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="63c59-117">**Defina una extensión de nombre de archivo para el nuevo tipo de archivo.**</span><span class="sxs-lookup"><span data-stu-id="63c59-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="63c59-118">Los desarrolladores eligen `.opa-ltw-audio` , que incorpora su abreviatura de proveedor y una sugerencia sobre lo que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="63c59-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="63c59-119">La investigación determina que nadie más usa la extensión.</span><span class="sxs-lookup"><span data-stu-id="63c59-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="63c59-120">Siguiendo las recomendaciones actuales, no se define ninguna extensión corta.</span><span class="sxs-lookup"><span data-stu-id="63c59-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="63c59-121">**Defina un tipo MIME para el tipo de archivo y regístrelo con IANA.**</span><span class="sxs-lookup"><span data-stu-id="63c59-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="63c59-122">Litware define el nuevo tipo MIME como *audio/LitwarePlayer.1* y prepara una aplicación de tipo MIME, siguiendo las directrices establecidas en los números de solicitud de comentarios (RFC) 2045, 2046, 2047 y 2048.</span><span class="sxs-lookup"><span data-stu-id="63c59-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="63c59-123">A continuación, envían la aplicación a IANA, que agrega el nuevo tipo de archivo a la base de datos de tipos MIME registrados.</span><span class="sxs-lookup"><span data-stu-id="63c59-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="63c59-124">**Determine si existe un ProgID para el tipo de archivo.**</span><span class="sxs-lookup"><span data-stu-id="63c59-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="63c59-125">Dado que se trata de un nuevo tipo de archivo, no [existe ningún ProgID](fa-progids.md) para él.</span><span class="sxs-lookup"><span data-stu-id="63c59-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="63c59-126">Litware establece sobre el diseño de un nuevo ProgID para LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="63c59-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="63c59-127">Deciden el nombre descriptivo "LitwarePlayer Audio Player" (que se almacena como un recurso en el archivo LitwarePlayer.exe) y diseñan un icono predeterminado para usarlo para los archivos asociados a LitwarePlayer (también almacenados en LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="63c59-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="63c59-128">Dado que LitwarePlayer es una nueva aplicación, se trata de un ProgID de la versión 1.</span><span class="sxs-lookup"><span data-stu-id="63c59-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="63c59-129">**Registre el ProgID.**</span><span class="sxs-lookup"><span data-stu-id="63c59-129">**Register the ProgID.**</span></span> <span data-ttu-id="63c59-130">Cuando se instala LitwarePlayer, el programa de instalación crea la siguiente [entrada ProgID](fa-progids.md) en el Registro.</span><span class="sxs-lookup"><span data-stu-id="63c59-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="63c59-131">En la clave de comando, %1 se pasa como ruta de acceso al archivo que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="63c59-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="63c59-132">**Registre la extensión de nombre de archivo para el tipo de archivo.**</span><span class="sxs-lookup"><span data-stu-id="63c59-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="63c59-133">Cuando se instala LitwarePlayer, el programa de instalación crea las siguientes entradas en el Registro para su extensión de tipo de archivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="63c59-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="63c59-134">Siempre que se cree o cambie una asociación de archivos, notifique al sistema que se ha realizado un cambio mediante una llamada a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando el evento \_ ASSOCCHANGED de SHCNE.</span><span class="sxs-lookup"><span data-stu-id="63c59-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="63c59-135">Si esto no se hace, es posible que el Shell no reconozca los cambios realizados hasta que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="63c59-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="63c59-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63c59-136">Additional Resources</span></span>

-   [<span data-ttu-id="63c59-137">Introducción a las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="63c59-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="63c59-138">Cómo registrar un explorador de Internet o un cliente de correo electrónico con el menú Inicio de Windows</span><span class="sxs-lookup"><span data-stu-id="63c59-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="63c59-139">[Registro de una aplicación en un esquema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63c59-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="63c59-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63c59-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63c59-141">Procedimientos recomendados para asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="63c59-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="63c59-142">Directrices para administrar aplicaciones predeterminadas en Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="63c59-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="63c59-143">Programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="63c59-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="63c59-144">Establecer el acceso al programa y los valores predeterminados del equipo (SPAD)</span><span class="sxs-lookup"><span data-stu-id="63c59-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
