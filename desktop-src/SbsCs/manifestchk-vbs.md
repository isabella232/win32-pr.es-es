---
description: El archivo VBScript Manifestchk.vbs es una herramienta de validación proporcionada en el kit de desarrollo de software (SDK) de Microsoft Windows que valida los archivos de manifiesto de la aplicación y el ensamblado.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423863"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="1d105-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="1d105-103">Manifestchk.vbs</span></span>

<span data-ttu-id="1d105-104">El archivo VBScript Manifestchk.vbs es una herramienta de validación proporcionada en el kit de desarrollo de software (SDK) de Microsoft Windows que valida los archivos de manifiesto de la aplicación y el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="1d105-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="1d105-105">La ejecución de este ejemplo requiere Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="1d105-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="1d105-106">Para obtener más información acerca de Windows Script Host, consulte la sección Windows Script Host de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1d105-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="1d105-107">Windows Script Host es en realidad dos hosts.</span><span class="sxs-lookup"><span data-stu-id="1d105-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="1d105-108">CScript.exe es la versión que permite ejecutar scripts desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d105-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="1d105-109">CScript.exe proporciona modificadores de la línea de comandos para establecer las propiedades del script.</span><span class="sxs-lookup"><span data-stu-id="1d105-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="1d105-110">El formato de línea de comandos es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d105-110">The command-line format is the following:</span></span>

<span data-ttu-id="1d105-111">**Cscript el manifestchk.vbs/s:** *\[ unidad: \] \[ ruta de acceso \] schemafilename* **/m:** *\[ unidad: \] \[ ruta de acceso \] manifestfilename* **\[ /q \] /t:** *opción*</span><span class="sxs-lookup"><span data-stu-id="1d105-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="1d105-112">En la tabla siguiente se describen las marcas definidas para Manifestchk.vbs.</span><span class="sxs-lookup"><span data-stu-id="1d105-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="1d105-113">Marca</span><span class="sxs-lookup"><span data-stu-id="1d105-113">Flag</span></span> | <span data-ttu-id="1d105-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d105-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d105-115">/s</span><span class="sxs-lookup"><span data-stu-id="1d105-115">/s</span></span>   | <span data-ttu-id="1d105-116">Especifica el nombre del archivo de esquema de manifiesto con el que validar los manifiestos.</span><span class="sxs-lookup"><span data-stu-id="1d105-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="1d105-117">Vea el esquema en el [esquema del archivo de manifiesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="1d105-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="1d105-118">/m</span><span class="sxs-lookup"><span data-stu-id="1d105-118">/m</span></span>   | <span data-ttu-id="1d105-119">Especifica el nombre del archivo de manifiesto que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="1d105-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1d105-120">/q</span><span class="sxs-lookup"><span data-stu-id="1d105-120">/q</span></span>   | <span data-ttu-id="1d105-121">Suprime todos los resultados en la consola.</span><span class="sxs-lookup"><span data-stu-id="1d105-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1d105-122">/t</span><span class="sxs-lookup"><span data-stu-id="1d105-122">/t</span></span>   | <span data-ttu-id="1d105-123">Especifica el tipo de archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="1d105-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="1d105-124">Los valores válidos son: AM valida el [esquema del archivo de manifiesto](manifest-file-schema.md) de un manifiesto de [ensamblado](assembly-manifests.md) o un [manifiesto de aplicación](application-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="1d105-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="1d105-125">El equipo valida el [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md) de un archivo de configuración del [publicador](publisher-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="1d105-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="1d105-126">AC valide el esquema del archivo de configuración de la aplicación de un [archivo de configuración](application-configuration-files.md)de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d105-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="1d105-127">Si no se especifica la marca/q, Manifestchk.vbs muestra información detallada acerca del primer error encontrado en el archivo y muestra un mensaje que indica si el proceso de validación se realizó correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="1d105-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="1d105-128">Esta utilidad comprueba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d105-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="1d105-129">Una línea de comandos válida.</span><span class="sxs-lookup"><span data-stu-id="1d105-129">A valid command line.</span></span>
-   <span data-ttu-id="1d105-130">Está instalada la versión 3 de MSXML.</span><span class="sxs-lookup"><span data-stu-id="1d105-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="1d105-131">Que el manifiesto usa XML con formato correcto.</span><span class="sxs-lookup"><span data-stu-id="1d105-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="1d105-132">Que el manifiesto acepta con el esquema proporcionado.</span><span class="sxs-lookup"><span data-stu-id="1d105-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="1d105-133">Tenga en cuenta que Manifestchk.vbs comprueba el archivo de manifiesto basándose solo en lo que se especifica en el esquema proporcionado.</span><span class="sxs-lookup"><span data-stu-id="1d105-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="1d105-134">Para ver un ejemplo de un esquema de manifiesto, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="1d105-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="1d105-135">Cscript.exe devuelve un valor de 0 si el proceso de validación se realizó correctamente y 1 si no se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d105-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="1d105-136">Devuelve 2 si hay un error en un argumento de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1d105-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d105-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d105-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d105-138">Herramientas de desarrollo de ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="1d105-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




