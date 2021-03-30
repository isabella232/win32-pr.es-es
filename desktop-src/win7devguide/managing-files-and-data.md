---
title: Administrar archivos y datos
description: Los usuarios tienen un acceso más sencillo a los archivos y datos en Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995409"
---
# <a name="managing-files-and-data"></a><span data-ttu-id="aa648-103">Administrar archivos y datos</span><span class="sxs-lookup"><span data-stu-id="aa648-103">Managing Files and Data</span></span>

<span data-ttu-id="aa648-104">Los usuarios tienen un acceso más sencillo a los archivos y datos en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa648-104">Users have easier access to files and data in Windows 7.</span></span> <span data-ttu-id="aa648-105">Las nuevas API hacen que los archivos y las vistas sean más informativos, lo que permite a las aplicaciones ofrecer información relevante e distintiva al explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="aa648-105">New APIs make files and views more informative, enabling applications to deliver relevant and distinctive information to Windows Explorer.</span></span> <span data-ttu-id="aa648-106">Además, las aplicaciones se benefician del nuevo modelo de *bibliotecas* , una noción útil y más abstracta del espacio de almacenamiento de usuario que las carpetas, y también pueden participar en bibliotecas comunes de tipos de archivo similares compartidos por aplicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="aa648-106">In addition, applications benefit from the new *Libraries* model, a useful, more abstract notion of user storage space than folders, and can also participate in common libraries of similar file types that are shared by different applications.</span></span>

## <a name="libraries"></a><span data-ttu-id="aa648-107">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="aa648-107">Libraries</span></span>

<span data-ttu-id="aa648-108">Windows 7 presenta el concepto de *bibliotecas* como destinos en los que los desarrolladores y los usuarios finales pueden buscar y organizar sus datos como colecciones de elementos que pueden abarcar varias ubicaciones en el equipo local, así como en equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="aa648-108">Windows 7 introduces the concept of *Libraries* as destinations where developers and end-users can find and organize their data as collections of items that can span multiple locations on the local computer as well as on remote computers.</span></span>

<span data-ttu-id="aa648-109">Las API de *biblioteca* proporcionan a los desarrolladores una forma sencilla de crear aplicaciones que crean, interactúan con las bibliotecas y admiten *bibliotecas* como elementos de primera clase dentro de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="aa648-109">The *Library* APIs provide a straightforward way for developers to create applications that create, interact with, and support *Libraries* as first-class items within applications.</span></span> <span data-ttu-id="aa648-110">Las *bibliotecas* también se pueden seleccionar mediante el cuadro de diálogo Selector de carpetas.</span><span class="sxs-lookup"><span data-stu-id="aa648-110">*Libraries* can also be selected by using the folder picker dialog box.</span></span> <span data-ttu-id="aa648-111">Las aplicaciones pueden enumerar ámbitos de biblioteca relevantes o pueden utilizar la biblioteca directamente como una carpeta.</span><span class="sxs-lookup"><span data-stu-id="aa648-111">Applications can enumerate relevant library scopes, or they can use the library directly as a folder.</span></span> <span data-ttu-id="aa648-112">(Consulte [bibliotecas de Windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) y [bibliotecas de Windows 7: recursos para desarrolladores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span><span class="sxs-lookup"><span data-stu-id="aa648-112">(See [Windows Libraries](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) and [Windows 7 Libraries: Developer Resources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span></span>

![Biblioteca de imágenes de Windows 7](images/windows7-10.jpg)

<span data-ttu-id="aa648-114">La *biblioteca de imágenes* muestra las imágenes independientemente de dónde estén almacenadas</span><span class="sxs-lookup"><span data-stu-id="aa648-114">*Pictures Library* shows your pictures no matter where they are stored</span></span>

## <a name="file-formats-and-data-stores"></a><span data-ttu-id="aa648-115">Formatos de archivo y almacenes de datos</span><span class="sxs-lookup"><span data-stu-id="aa648-115">File Formats and Data Stores</span></span>

<span data-ttu-id="aa648-116">En Windows 7, el explorador de Windows facilita la administración de archivos y la manipulación para el usuario de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="aa648-116">In Windows 7, Windows Explorer makes file management and manipulation easier for the user in several ways:</span></span>

-   <span data-ttu-id="aa648-117">La vista previa del tipo de archivo de la aplicación es más accesible con un botón nuevo que permite a los usuarios mostrar y ocultar el panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="aa648-117">The preview for your application's file type is more accessible with a new button that lets users show and hide the preview pane.</span></span>
-   <span data-ttu-id="aa648-118">Las pilas visuales envolventes agregan imágenes en miniatura para los tipos de archivo en una vista.</span><span class="sxs-lookup"><span data-stu-id="aa648-118">Immersive visual stacks aggregate thumbnail images for file types in a view.</span></span>
-   <span data-ttu-id="aa648-119">Las vistas del explorador de Windows muestran información útil basada en las propiedades escritas con el controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="aa648-119">Windows Explorer views show useful information based on properties written with your property handler.</span></span>
-   <span data-ttu-id="aa648-120">Fragmentos de código de documento y resaltado de referencias use la implementación de la interfaz de **IFilter** para facilitar la búsqueda y la búsqueda de archivos.</span><span class="sxs-lookup"><span data-stu-id="aa648-120">Document snippets and hit highlighting use your **IFilter** interface implementation to make searching and finding files easier.</span></span>
-   <span data-ttu-id="aa648-121">Los comandos y verbos de menú contextual son más fáciles de implementar.</span><span class="sxs-lookup"><span data-stu-id="aa648-121">Context-menu verbs and commands are easier than ever to implement.</span></span>

<span data-ttu-id="aa648-122">Al implementar todos los controladores de formato adecuados para los elementos devueltos por el controlador de protocolo, los resultados de la búsqueda del almacén de datos personalizado pueden ser tan completos como los resultados de la búsqueda de archivos.</span><span class="sxs-lookup"><span data-stu-id="aa648-122">By implementing all of the appropriate format handlers for the items returned from your protocol handler, search results from your custom data store can be as rich as search results from files.</span></span> <span data-ttu-id="aa648-123">Las *bibliotecas* se crean automáticamente para los controladores de protocolo, por lo que los usuarios pueden limitar sus búsquedas fácilmente.</span><span class="sxs-lookup"><span data-stu-id="aa648-123">*Libraries* are automatically created for your protocol handlers so users can scope their searches easily.</span></span> <span data-ttu-id="aa648-124">Y la lógica para crear *bibliotecas* se puede personalizar fácilmente a través del registro.</span><span class="sxs-lookup"><span data-stu-id="aa648-124">And the logic for creating *Libraries* can be easily customized through the registry.</span></span> <span data-ttu-id="aa648-125">(Consulte [desarrollo de filtros para Windows Search](../search/-search-3x-wds-extidx-filters.md)).</span><span class="sxs-lookup"><span data-stu-id="aa648-125">(See [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span></span>

![Biblioteca de documentos de Windows 7](images/windows7-11.jpg)

<span data-ttu-id="aa648-127">En Windows 7, el explorador de Windows facilita la administración y manipulación de archivos</span><span class="sxs-lookup"><span data-stu-id="aa648-127">In Windows 7, Windows Explorer makes file management and manipulation easier</span></span>

 

 