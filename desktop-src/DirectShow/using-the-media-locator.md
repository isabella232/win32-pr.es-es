---
description: Usar el localizador de medios
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Usar el localizador de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003313"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="84e98-103">Usar el localizador de medios</span><span class="sxs-lookup"><span data-stu-id="84e98-103">Using the Media Locator</span></span>

<span data-ttu-id="84e98-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="84e98-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="84e98-105">El localizador multimedia es un objeto auxiliar que comprueba los nombres de archivo y busca archivos que faltan en directorios locales o de red.</span><span class="sxs-lookup"><span data-stu-id="84e98-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="84e98-106">El detector de medios mantiene una memoria caché de rutas de acceso de directorio donde ha encontrado correctamente archivos en búsquedas anteriores.</span><span class="sxs-lookup"><span data-stu-id="84e98-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="84e98-107">Para buscar un archivo, busca en los directorios de su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="84e98-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="84e98-108">En caso de error, el detector de medios puede mostrar un cuadro de diálogo Abrir archivo para que el usuario busque un archivo manualmente.</span><span class="sxs-lookup"><span data-stu-id="84e98-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="84e98-109">Suponiendo que el usuario busque el archivo, el localizador de medios agrega el nuevo directorio a su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="84e98-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="84e98-110">El localizador de medios expone la interfaz [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="84e98-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="84e98-111">Normalmente, la aplicación no crea directamente una instancia del localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="84e98-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="84e98-112">En su lugar, la escala de tiempo y el motor de representación proporcionan los siguientes métodos para validar nombres de archivo mediante el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="84e98-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="84e98-113">Para validar los nombres de archivo en la escala de tiempo, llame a [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span><span class="sxs-lookup"><span data-stu-id="84e98-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="84e98-114">Opcionalmente, este método también actualiza los objetos de origen con los nombres de archivo correctos.</span><span class="sxs-lookup"><span data-stu-id="84e98-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="84e98-115">Para validar los nombres de archivo cuando se representa el proyecto, llame a [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span><span class="sxs-lookup"><span data-stu-id="84e98-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="84e98-116">Ambos métodos toman marcas que controlan el comportamiento del localizador de medios.</span><span class="sxs-lookup"><span data-stu-id="84e98-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="84e98-117">Por ejemplo, puede restringir la búsqueda a directorios locales.</span><span class="sxs-lookup"><span data-stu-id="84e98-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84e98-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84e98-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84e98-119">Trabajar con orígenes</span><span class="sxs-lookup"><span data-stu-id="84e98-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



