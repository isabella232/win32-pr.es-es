---
description: El grupo de archivos de tablas contiene todas las tablas de Windows Installer que están relacionadas con los archivos.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Grupo de tablas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687185"
---
# <a name="file-tables-group"></a><span data-ttu-id="366ce-103">Grupo de tablas de archivos</span><span class="sxs-lookup"><span data-stu-id="366ce-103">File Tables Group</span></span>

![Grupo de tablas de archivos](images/filegrp.png)

<span data-ttu-id="366ce-105">Para obtener más información sobre este diagrama, vea la [leyenda del diagrama de relaciones de entidades](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="366ce-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="366ce-106">Un desarrollador de paquetes de instalador debe considerar la posibilidad de rellenar el grupo de tablas de archivos después de dividir la aplicación en [componentes y características](components-and-features.md) y después de rellenar el [grupo de tablas principales](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="366ce-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="366ce-107">El grupo de tabla de archivos contiene todos los archivos que pertenecen a la instalación y la mayoría de estos archivos se enumeran en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="366ce-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="366ce-108">La [tabla de directorio](directory-table.md) no se muestra en la figura, pero está estrechamente relacionada con el grupo de tablas de archivos.</span><span class="sxs-lookup"><span data-stu-id="366ce-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="366ce-109">La tabla del directorio proporciona la estructura de directorios de la instalación.</span><span class="sxs-lookup"><span data-stu-id="366ce-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="366ce-110">El grupo de archivos de tablas contiene todas las tablas que están relacionadas con los archivos.</span><span class="sxs-lookup"><span data-stu-id="366ce-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="366ce-111">La [tabla de archivos](file-table.md) muestra los archivos que pertenecen a la instalación.</span><span class="sxs-lookup"><span data-stu-id="366ce-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="366ce-112">Los archivos que no aparecen en la tabla de archivos incluyen archivos de disco, que se enumeran en la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="366ce-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="366ce-113">Dado que cada archivo pertenece a un componente, la tabla de archivos tiene una clave externa en la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="366ce-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="366ce-114">La [tabla RemoveFile](removefile-table.md) contiene una lista de archivos que se van a quitar mediante la [acción RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="366ce-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="366ce-115">La [tabla fuente](font-table.md) muestra los archivos de fuente que se van a registrar con el sistema.</span><span class="sxs-lookup"><span data-stu-id="366ce-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="366ce-116">En la [tabla SelfReg](selfreg-table.md) se muestran los archivos de módulo de la instalación que se han registrado automáticamente.</span><span class="sxs-lookup"><span data-stu-id="366ce-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="366ce-117">En la [tabla de medios](media-table.md) se enumeran los medios de origen y los discos que pertenecen a la instalación.</span><span class="sxs-lookup"><span data-stu-id="366ce-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="366ce-118">En la [tabla BindImage](bindimage-table.md) se muestran los archivos que están enlazados a archivos dll importados por ejecutables.</span><span class="sxs-lookup"><span data-stu-id="366ce-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="366ce-119">La [tabla MoveFile](movefile-table.md) especifica qué archivos se mueven durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="366ce-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="366ce-120">La [tabla DuplicateFile](duplicatefile-table.md) especifica los archivos que se van a duplicar durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="366ce-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="366ce-121">La [tabla inifile](inifile-table.md) enumera los archivos. ini y la información que la aplicación necesita para establecer en el archivo.</span><span class="sxs-lookup"><span data-stu-id="366ce-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="366ce-122">La [tabla RemoveIniFile](removeinifile-table.md) contiene la información que debe eliminar una aplicación de un archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="366ce-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="366ce-123">La [tabla de entorno](environment-table.md) se utiliza para establecer los valores de las variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="366ce-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="366ce-124">La [tabla de iconos](icon-table.md) proporciona información de iconos que se copia en un archivo como parte del anuncio del producto.</span><span class="sxs-lookup"><span data-stu-id="366ce-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="366ce-125">La [tabla FileSFPCatalog](filesfpcatalog-table.md) asocia los archivos especificados con los archivos de catálogo de protección de archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="366ce-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="366ce-126">**Windows Vista, Windows Server 2003 y Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="366ce-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="366ce-127">La [tabla SFPCatalog](sfpcatalog-table.md) contiene catálogos de protección de archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="366ce-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="366ce-128">**Windows Vista, Windows Server 2003 y Windows XP:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="366ce-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="366ce-129">La [tabla MsiFileHash](msifilehash-table.md) se usa para almacenar un hash de 128 bits de un archivo de código fuente proporcionado por el paquete Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="366ce-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 



