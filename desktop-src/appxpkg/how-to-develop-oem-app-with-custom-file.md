---
title: Cómo desarrollar una aplicación de OEM que use un archivo personalizado
description: Obtenga información sobre cómo desarrollar una aplicación que use un archivo personalizado para pasar información del OEM a la aplicación.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105704933"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="c8912-103">Cómo desarrollar una aplicación de OEM que use un archivo personalizado</span><span class="sxs-lookup"><span data-stu-id="c8912-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="c8912-104">Para obtener más información sobre la creación y el uso de archivos de datos personalizados, consulte [Opciones de mantenimiento del paquete de aplicación de DISM (. appx o. appxbundle) Command-Line](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span><span class="sxs-lookup"><span data-stu-id="c8912-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="c8912-105">Obtenga información sobre cómo desarrollar una aplicación que use un archivo personalizado para pasar información del OEM a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8912-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="c8912-106">En el caso de las aplicaciones que cree para la implementación de OEM, puede usar un archivo personalizado para pasar información del OEM a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c8912-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="c8912-107">Para pasar información de OEM a una aplicación, cree un archivo. Data personalizado en la carpeta microsoft.sysTEM. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="c8912-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="c8912-108">Este nombre de archivo es especial para el sistema operativo y se realiza automáticamente durante las actualizaciones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8912-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="c8912-109">Los OEM pueden usar este archivo para pasar identificadores personalizados, de modo que las aplicaciones sepan cuándo han implementado los OEM.</span><span class="sxs-lookup"><span data-stu-id="c8912-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="c8912-110">Solo puede tener un archivo. Data personalizado por aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8912-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="c8912-111">Las aplicaciones deben poder buscar y leer este archivo correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8912-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="c8912-112">Los desarrolladores tratan el archivo como datos que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="c8912-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c8912-113">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="c8912-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c8912-114">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="c8912-114">Technologies</span></span>

-   [<span data-ttu-id="c8912-115">Inicio rápido: información del manifiesto del paquete de la aplicación de consulta</span><span class="sxs-lookup"><span data-stu-id="c8912-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="c8912-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c8912-116">Prerequisites</span></span>

-   <span data-ttu-id="c8912-117">Necesita la herramienta [Administración y mantenimiento de imágenes de implementación (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) para agregar el paquete de la aplicación con el archivo de datos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8912-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="c8912-118">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c8912-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="c8912-119">Paso 1: crear un archivo personalizado y agregarlo a la carpeta de metadatos del paquete</span><span class="sxs-lookup"><span data-stu-id="c8912-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="c8912-120">Puede diseñar la aplicación para que use cualquier formato que elija para los datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="c8912-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="c8912-121">Por ejemplo, puede usar XML, un archivo de texto u otro tipo de archivo para organizar los datos.</span><span class="sxs-lookup"><span data-stu-id="c8912-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="c8912-122">Le recomendamos que considere cómo puede probar y validar el archivo.</span><span class="sxs-lookup"><span data-stu-id="c8912-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="c8912-123">Por ejemplo, puede crear un esquema XML para validar un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="c8912-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="c8912-124">Puede especificar cualquier tipo de archivo con cualquier nombre de archivo para los datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="c8912-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="c8912-125">Al agregar el paquete de la aplicación con el archivo de datos personalizado mediante la herramienta [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , DISM cambia el nombre del archivo personalizado a Custom. Data y guarda el archivo en la carpeta microsoft.sysTEM. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="c8912-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="c8912-126">La aplicación no puede modificar el archivo de datos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8912-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="c8912-127">Es un recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8912-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="c8912-128">Paso 2: acceder al archivo de datos personalizado para una aplicación</span><span class="sxs-lookup"><span data-stu-id="c8912-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="c8912-129">Puede tener acceso al archivo. Data personalizado para una aplicación desde el código mediante las API de Windows para obtener información del paquete actual.</span><span class="sxs-lookup"><span data-stu-id="c8912-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="c8912-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c8912-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="c8912-131">Para obtener más información sobre el desarrollo con la propiedad [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , consulte [Inicio rápido: información del manifiesto del paquete](how-to-query-package-identity-information.md)de la aplicación de consulta.</span><span class="sxs-lookup"><span data-stu-id="c8912-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="c8912-132">Para obtener más información sobre el acceso al archivo. Data personalizado a través de [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) y el uso de objetos [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , vea [acceso a datos y archivos](/previous-versions/windows/apps/hh464959(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="c8912-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8912-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8912-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8912-134">Inicio rápido: información del manifiesto del paquete de la aplicación de consulta</span><span class="sxs-lookup"><span data-stu-id="c8912-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 