---
description: Los desarrolladores crean un paquete de revisión generando un archivo de creación de revisiones y usando Msimsp.exe para llamar a la función UiCreatePatchPackageEx en Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Crear un paquete de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277185"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="c6e80-103">Crear un paquete de revisión</span><span class="sxs-lookup"><span data-stu-id="c6e80-103">Creating a Patch Package</span></span>

<span data-ttu-id="c6e80-104">Los desarrolladores crean un paquete de revisión generando un archivo de creación de revisiones y usando [Msimsp.exe](msimsp-exe.md) para llamar a la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) en [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="c6e80-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="c6e80-105">En el SDK de Windows Installer se proporcionan Msimsp.exe y Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="c6e80-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="c6e80-106">Para obtener más información, vea [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="c6e80-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="c6e80-107">Dado que la aplicación de una revisión a un paquete de Windows Installer da como resultado la instalación de los orígenes originales con un nuevo archivo. msi, el nuevo archivo. msi debe ser compatible con el diseño del origen original.</span><span class="sxs-lookup"><span data-stu-id="c6e80-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="c6e80-108">Cuando cree un paquete de revisión, debe utilizar una imagen de instalación sin comprimir para crear una revisión, por ejemplo, una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="c6e80-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="c6e80-109">También debe cumplir las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6e80-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="c6e80-110">No mueva archivos de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="c6e80-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="c6e80-111">No mueva archivos de un archivo. cab a otro.</span><span class="sxs-lookup"><span data-stu-id="c6e80-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="c6e80-112">No cambie el orden de los archivos en un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="c6e80-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="c6e80-113">No cambie el número de secuencia de los archivos existentes.</span><span class="sxs-lookup"><span data-stu-id="c6e80-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="c6e80-114">El número de secuencia es el valor especificado en la columna Sequence de la [tabla File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="c6e80-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="c6e80-115">Los archivos nuevos que agregue la revisión deben colocarse al final de la secuencia de archivos existente.</span><span class="sxs-lookup"><span data-stu-id="c6e80-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="c6e80-116">El número de secuencia de cualquier archivo nuevo en la imagen actualizada debe ser mayor que el número de secuencia más grande de los archivos existentes en la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="c6e80-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="c6e80-117">No cambie las claves principales de la [tabla de archivos](file-table.md) entre las versiones originales y nuevas del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="c6e80-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="c6e80-118">El archivo debe tener la misma clave en la [tabla de archivos](file-table.md) de la imagen de destino y la imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="c6e80-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="c6e80-119">Los valores de cadena de la columna de archivo de ambas tablas deben ser idénticos, incluido el caso.</span><span class="sxs-lookup"><span data-stu-id="c6e80-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="c6e80-120">No cree un paquete con claves de [tabla de archivos](file-table.md) que solo difieran en caso de que, por ejemplo, evite el siguiente ejemplo de tabla.</span><span class="sxs-lookup"><span data-stu-id="c6e80-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="c6e80-121">Archivo</span><span class="sxs-lookup"><span data-stu-id="c6e80-121">File</span></span>       | <span data-ttu-id="c6e80-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c6e80-122">Component\_</span></span> | <span data-ttu-id="c6e80-123">FileName</span><span class="sxs-lookup"><span data-stu-id="c6e80-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="c6e80-124">readme.txt</span><span class="sxs-lookup"><span data-stu-id="c6e80-124">readme.txt</span></span> | <span data-ttu-id="c6e80-125">Comp1</span><span class="sxs-lookup"><span data-stu-id="c6e80-125">Comp1</span></span>       | <span data-ttu-id="c6e80-126">readme.txt</span><span class="sxs-lookup"><span data-stu-id="c6e80-126">readme.txt</span></span> |
    | <span data-ttu-id="c6e80-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="c6e80-127">ReadMe.txt</span></span> | <span data-ttu-id="c6e80-128">Comp2</span><span class="sxs-lookup"><span data-stu-id="c6e80-128">Comp2</span></span>       | <span data-ttu-id="c6e80-129">readme.txt</span><span class="sxs-lookup"><span data-stu-id="c6e80-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="c6e80-130">El Windows Installer puede permitir el ejemplo de tabla anterior cuando Comp1 y Comp2 se instalan en directorios diferentes, pero no puede usar [Msimsp.exe](msimsp-exe.md) o [Patchwiz.dll](patchwiz-dll.md) para generar una revisión para el paquete.</span><span class="sxs-lookup"><span data-stu-id="c6e80-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="c6e80-131">Msimsp.exe y Patchwiz.dll llaman a Makecab.exe, que distingue entre mayúsculas y minúsculas y produce un error.</span><span class="sxs-lookup"><span data-stu-id="c6e80-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="c6e80-132">Al usar módulos de fusión mediante combinación en el programa de instalación, asegúrese de que los números de secuencia de archivos y el diseño cumplen las instrucciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c6e80-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 



