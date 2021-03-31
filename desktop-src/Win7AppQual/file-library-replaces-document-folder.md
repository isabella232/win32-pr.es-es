---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La biblioteca de archivos reemplaza a la carpeta de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912758"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="5eb95-103">La biblioteca de archivos reemplaza a la carpeta de documentos</span><span class="sxs-lookup"><span data-stu-id="5eb95-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="5eb95-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="5eb95-104">Affected Platforms</span></span>

<span data-ttu-id="5eb95-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="5eb95-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="5eb95-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5eb95-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="5eb95-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="5eb95-107">Feature Impact</span></span>

<span data-ttu-id="5eb95-108">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="5eb95-108">**Severity** - Medium</span></span>  
<span data-ttu-id="5eb95-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="5eb95-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="5eb95-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5eb95-110">Description</span></span>

<span data-ttu-id="5eb95-111">Las bibliotecas proporcionan una experiencia de tipo carpeta centralizada para el almacenamiento de archivos, la búsqueda y el acceso a través de varias ubicaciones, tanto locales como remotas.</span><span class="sxs-lookup"><span data-stu-id="5eb95-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="5eb95-112">Las ubicaciones predeterminadas que usan los cuadros de diálogo de archivos comunes (por ejemplo, abrir y guardar) se han cambiado de la carpeta de documentos a la biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="5eb95-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="5eb95-113">La interfaz de usuario no ha cambiado, pero el usuario podrá ver, examinar y buscar en la biblioteca mediante varias vistas de organización.</span><span class="sxs-lookup"><span data-stu-id="5eb95-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="5eb95-114">Los archivos se guardarán en la ubicación de almacenamiento predeterminada de la biblioteca, a menos que el usuario cambie la ubicación de almacenamiento predeterminada o elija otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="5eb95-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="5eb95-115">Los desarrolladores pueden crear sus propias bibliotecas o agregar ubicaciones a las bibliotecas existentes mediante la interfaz IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="5eb95-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="5eb95-116">Los usuarios pueden encontrar bibliotecas mediante el sistema de carpetas conocido (por ejemplo, FOLDERID \_ DocumentsLibrary).</span><span class="sxs-lookup"><span data-stu-id="5eb95-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="5eb95-117">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="5eb95-117">Manifestation of Impact</span></span>

<span data-ttu-id="5eb95-118">La biblioteca es un archivo, no una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5eb95-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="5eb95-119">Por lo tanto, las manipulaciones de ruta de acceso podrían producir errores debido al intento de la aplicación de concatenar archivos en los archivos.</span><span class="sxs-lookup"><span data-stu-id="5eb95-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="5eb95-120">Solución</span><span class="sxs-lookup"><span data-stu-id="5eb95-120">Solution</span></span>

<span data-ttu-id="5eb95-121">Al usar IFileDialog, debe usar el método GetResult en lugar de la combinación de GetFolder y GetFilename, tal como lo haría en las versiones anteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5eb95-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="5eb95-122">Use las API de Shell donde sea posible para interactuar con los elementos del espacio de nombres del shell y manipularlos (por ejemplo, IShellItem).</span><span class="sxs-lookup"><span data-stu-id="5eb95-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="5eb95-123">Aprovechar las capacidades de características</span><span class="sxs-lookup"><span data-stu-id="5eb95-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="5eb95-124">Si desea crear sus propias bibliotecas o agregar ubicaciones a las bibliotecas existentes, debe usar la API de IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="5eb95-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="5eb95-125">Las bibliotecas son carpetas de Shell, por lo que puede enumerarlas como cualquier otra carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="5eb95-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="5eb95-126">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="5eb95-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="5eb95-127">Al usar el cuadro de diálogo archivo común, se asegurará de que los usuarios pueden guardar directamente en sus bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="5eb95-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="5eb95-128">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="5eb95-128">Links to Other Resources</span></span>

-   <span data-ttu-id="5eb95-129">**Bibliotecas de Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="5eb95-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="5eb95-130">**Mantener la sincronización con una biblioteca:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="5eb95-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



