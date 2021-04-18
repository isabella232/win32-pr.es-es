---
description: El WiLstPrd.vbs de archivos de VBScript se proporciona en los componentes de Windows SDK para Windows Installer desarrolladores. El script de ejemplo se conecta a un objeto de instalador y enumera los productos registrados y la información del producto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Enumerar productos, propiedades, características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686796"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="5c7ac-104">Enumerar productos, propiedades, características y componentes</span><span class="sxs-lookup"><span data-stu-id="5c7ac-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="5c7ac-105">El WiLstPrd.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5c7ac-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="5c7ac-106">El script de ejemplo se conecta a un objeto de [**instalador**](installer-object.md) y enumera los productos registrados y la información del producto.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="5c7ac-107">Este ejemplo muestra el uso de:</span><span class="sxs-lookup"><span data-stu-id="5c7ac-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="5c7ac-108">**Propiedad ProductInfo**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="5c7ac-109">**Propiedad ProductState (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="5c7ac-110">**Propiedad Products**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="5c7ac-111">**Propiedad Features**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="5c7ac-112">**Propiedad FeatureParent**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="5c7ac-113">**Propiedad FeatureState**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="5c7ac-114">**Propiedad Components**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="5c7ac-115">**Propiedad ComponentClients**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="5c7ac-116">**Propiedad ComponentPath**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="5c7ac-117">**Método LastErrorRecord**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="5c7ac-118">[**Método**](installer-registryvalue.md) del objeto del [ **instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="5c7ac-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="5c7ac-119">Para usar este ejemplo, necesitará la versión CScript.exe o WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="5c7ac-120">Para usar CScript.exe para ejecutar este ejemplo, escriba una línea de comandos en el símbolo del sistema con la siguiente sintaxis.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="5c7ac-121">La ayuda se muestra si el primer argumento es/?</span><span class="sxs-lookup"><span data-stu-id="5c7ac-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="5c7ac-122">o si se especifican pocos argumentos.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-122">or if too few arguments are specified.</span></span> <span data-ttu-id="5c7ac-123">Para redirigir la salida a un archivo, finalice la línea de comandos con VBS > \[ ruta de acceso al archivo \] .</span><span class="sxs-lookup"><span data-stu-id="5c7ac-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="5c7ac-124">El ejemplo devuelve un valor de 0 para Success, 1 si se invoca la ayuda y 2 si se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="5c7ac-125">**cscript WiLstPrd.vbs \[ Opciones de nombre de producto \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="5c7ac-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="5c7ac-126">Especifique el nombre de producto sin distinción de mayúsculas y minúsculas o el GUID de ID. de producto del producto instalado o anunciado.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="5c7ac-127">Si no se especifica ningún producto o opción, el instalador muestra todos los productos instalados o anunciados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="5c7ac-128">Tenga en cuenta que estas opciones no son modificadores, por lo que no debe prefijarse con una barra diagonal (/) en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="5c7ac-129">Las siguientes opciones se pueden combinar mediante la concatenación de las letras.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="5c7ac-130">Por ejemplo, "PC" para mostrar las propiedades de los productos y los componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="5c7ac-131">Opción</span><span class="sxs-lookup"><span data-stu-id="5c7ac-131">Option</span></span>               | <span data-ttu-id="5c7ac-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c7ac-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7ac-133">no se especificaron opciones</span><span class="sxs-lookup"><span data-stu-id="5c7ac-133">no options specified</span></span> | <span data-ttu-id="5c7ac-134">Enumera las propiedades de los productos.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="5c7ac-135">p</span><span class="sxs-lookup"><span data-stu-id="5c7ac-135">p</span></span>                    | <span data-ttu-id="5c7ac-136">Enumera las propiedades de los productos.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="5c7ac-137">f</span><span class="sxs-lookup"><span data-stu-id="5c7ac-137">f</span></span>                    | <span data-ttu-id="5c7ac-138">Enumerar las características de los productos, los padres de características y los Estados de instalación</span><span class="sxs-lookup"><span data-stu-id="5c7ac-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="5c7ac-139">c</span><span class="sxs-lookup"><span data-stu-id="5c7ac-139">c</span></span>                    | <span data-ttu-id="5c7ac-140">Enumera los componentes instalados de los productos.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="5c7ac-141">d</span><span class="sxs-lookup"><span data-stu-id="5c7ac-141">d</span></span>                    | <span data-ttu-id="5c7ac-142">Enumere el valor bajo **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** para los archivos de claves del componente de los productos.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="5c7ac-143">Para obtener más información, vea [ejemplos de scripting de Windows Installer](windows-installer-scripting-examples.md) para obtener ejemplos adicionales de scripting.</span><span class="sxs-lookup"><span data-stu-id="5c7ac-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="5c7ac-144">Para ver utilidades de ejemplo que no requieren Windows Script Host, vea [Windows Installer herramientas de desarrollo](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5c7ac-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



