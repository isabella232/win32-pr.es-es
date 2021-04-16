---
description: El método recomendado para generar un paquete de revisión es usar herramientas de creación de revisiones como Msimsp.exe y Patchwiz.dll. La herramienta Msimsp.exe solo está disponible en los componentes de Windows SDK para Windows Installer desarrolladores.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678657"
---
# <a name="msimspexe"></a><span data-ttu-id="fc8ff-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="fc8ff-104">Msimsp.exe</span></span>

<span data-ttu-id="fc8ff-105">El método recomendado para generar un paquete de revisión es usar herramientas de creación de revisiones como Msimsp.exe y [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="fc8ff-106">La herramienta Msimsp.exe solo está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="fc8ff-107">Msimsp.exe es un archivo ejecutable que llama a [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="fc8ff-108">La herramienta se puede usar para crear un paquete de revisión pasando la ruta de acceso a un archivo de propiedades de creación de revisiones (archivo. PCP) y la ruta de acceso al paquete de revisión que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="fc8ff-109">Msimsp. ex también puede usarse para crear un archivo de registro y especificar una carpeta temporal en la que se guardan las transformaciones, los archivadores y los archivos que se usan para crear el paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="fc8ff-110">La sintaxis de línea de comandos para Msimsp.exe es:</span><span class="sxs-lookup"><span data-stu-id="fc8ff-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="fc8ff-111">Ruta de acceso **Msimsp.exe-s** *\[ al archivo \] . PCP* **-p** *\[ ruta de acceso \] al archivo. MSP* **{Options}**</span><span class="sxs-lookup"><span data-stu-id="fc8ff-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="fc8ff-112">Las opciones de línea de comandos no distinguen mayúsculas de minúsculas y se pueden usar delimitadores de barras diagonales en lugar de guiones.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="fc8ff-113">Si no se especifican opciones, Msimsp.exe muestra los valores actuales de las propiedades de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc8ff-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ ruta de acceso al archivo \] . PCP_</span><span class="sxs-lookup"><span data-stu-id="fc8ff-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-115">Esto es necesario y debe ir seguido de la ruta de acceso al archivo de propiedades de creación de revisiones (extensión. PCP).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="fc8ff-116">Para obtener más información, vea [PatchWiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_ruta de acceso al archivo. MSP_</span><span class="sxs-lookup"><span data-stu-id="fc8ff-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-118">Esto es necesario y va seguido de la ruta de acceso al paquete de revisión que se va a crear (extensión. msp).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_ruta de acceso a la carpeta temporal_</span><span class="sxs-lookup"><span data-stu-id="fc8ff-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-120">Optional.</span></span> <span data-ttu-id="fc8ff-121">Seguido de la ruta de acceso a la carpeta temporal.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="fc8ff-122">La ubicación predeterminada es% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="fc8ff-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="fc8ff-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-124">Optional.</span></span> <span data-ttu-id="fc8ff-125">Se produce un error si la carpeta temporal ya existe.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_ruta de acceso al archivo de registro_</span><span class="sxs-lookup"><span data-stu-id="fc8ff-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-127">Optional.</span></span> <span data-ttu-id="fc8ff-128">Seguido de la ruta de acceso al archivo de registro que describe el proceso de creación de la revisión y los errores.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="fc8ff-129">Para obtener más información, vea [valores devueltos para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ff-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-la ruta de acceso LP**_al archivo de registro con datos de rendimiento_</span><span class="sxs-lookup"><span data-stu-id="fc8ff-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-131">Optional.</span></span> <span data-ttu-id="fc8ff-132">Seguido de la ruta de acceso al archivo de registro que describe el proceso de creación de la revisión y los errores.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="fc8ff-133">Esta opción escribe los datos de rendimiento en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-133">This option writes performance data to log file.</span></span> <span data-ttu-id="fc8ff-134">Esta opción requiere la versión 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-135"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="fc8ff-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-136">Optional.</span></span> <span data-ttu-id="fc8ff-137">Muestra un cuadro de diálogo si la creación de la revisión se completa correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ff-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="fc8ff-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ff-139">Muestra la ayuda de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="fc8ff-140">Se puede producir un error en Msimsp.exe cuando llama a Makecab.exe si hay valores en la columna de archivo de la [tabla de archivos](file-table.md) del paquete de instalación que solo difieren en mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="fc8ff-141">Windows Installer distingue entre mayúsculas y minúsculas y permite un paquete de instalación como en la tabla siguiente solo cuando Comp1 y Comp2 se instalan en directorios diferentes.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="fc8ff-142">Sin embargo, en este escenario no puede usar Msimsp.exe o [Patchwiz.dll](patchwiz-dll.md) para generar una revisión para el paquete, ya que Msimsp.exe y Patchwiz.dll llaman a Makecab.exe, que no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="fc8ff-143">Evite la creación de un paquete de instalación como la siguiente [tabla de archivos](file-table.md)parciales.</span><span class="sxs-lookup"><span data-stu-id="fc8ff-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="fc8ff-144">Archivo</span><span class="sxs-lookup"><span data-stu-id="fc8ff-144">File</span></span>       | <span data-ttu-id="fc8ff-145">Componente\_</span><span class="sxs-lookup"><span data-stu-id="fc8ff-145">Component\_</span></span> | <span data-ttu-id="fc8ff-146">FileName</span><span class="sxs-lookup"><span data-stu-id="fc8ff-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="fc8ff-147">readme.txt</span><span class="sxs-lookup"><span data-stu-id="fc8ff-147">readme.txt</span></span> | <span data-ttu-id="fc8ff-148">Comp1</span><span class="sxs-lookup"><span data-stu-id="fc8ff-148">Comp1</span></span>       | <span data-ttu-id="fc8ff-149">readme.txt</span><span class="sxs-lookup"><span data-stu-id="fc8ff-149">readme.txt</span></span> |
> | <span data-ttu-id="fc8ff-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="fc8ff-150">ReadMe.txt</span></span> | <span data-ttu-id="fc8ff-151">Comp2</span><span class="sxs-lookup"><span data-stu-id="fc8ff-151">Comp2</span></span>       | <span data-ttu-id="fc8ff-152">readme.txt</span><span class="sxs-lookup"><span data-stu-id="fc8ff-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="fc8ff-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc8ff-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc8ff-154">Crear un paquete de revisión</span><span class="sxs-lookup"><span data-stu-id="fc8ff-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="fc8ff-155">Un pequeño ejemplo de revisión de actualización</span><span class="sxs-lookup"><span data-stu-id="fc8ff-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="fc8ff-156">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fc8ff-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="fc8ff-157">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="fc8ff-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



