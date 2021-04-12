---
description: Muestra cómo crear una búsqueda con restricciones de consulta mediante el modelo de programación de Shell.
title: Ejemplo de carpeta de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277792"
---
# <a name="search-folder-sample"></a><span data-ttu-id="e11c1-103">Ejemplo de carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e11c1-103">Search Folder Sample</span></span>

<span data-ttu-id="e11c1-104">Muestra cómo crear una búsqueda con restricciones de consulta mediante el modelo de programación de Shell.</span><span class="sxs-lookup"><span data-stu-id="e11c1-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="e11c1-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="e11c1-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e11c1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e11c1-106">Description</span></span>](#description)
-   [<span data-ttu-id="e11c1-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11c1-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e11c1-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e11c1-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e11c1-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e11c1-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e11c1-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e11c1-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="e11c1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e11c1-111">Description</span></span>

<span data-ttu-id="e11c1-112">En este ejemplo se muestra cómo crear una búsqueda restringida mediante el uso de la interfaz [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) para construir un elemento de Shell de carpeta (un contenedor) que representa la consulta.</span><span class="sxs-lookup"><span data-stu-id="e11c1-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="e11c1-113">Los resultados se muestran mediante el cuadro de diálogo Abrir archivo.</span><span class="sxs-lookup"><span data-stu-id="e11c1-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="e11c1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11c1-114">Requirements</span></span>



| <span data-ttu-id="e11c1-115">Producto</span><span class="sxs-lookup"><span data-stu-id="e11c1-115">Product</span></span>                                | <span data-ttu-id="e11c1-116">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="e11c1-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e11c1-117">Windows</span><span class="sxs-lookup"><span data-stu-id="e11c1-117">Windows</span></span>                                | <span data-ttu-id="e11c1-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e11c1-118">Windows Vista</span></span>           |
| <span data-ttu-id="e11c1-119">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="e11c1-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e11c1-120">7.0</span><span class="sxs-lookup"><span data-stu-id="e11c1-120">7.0</span></span>                     |



 

<span data-ttu-id="e11c1-121">Para conocer los requisitos adicionales, consulte el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e11c1-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="e11c1-122">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e11c1-122">Downloading the Sample</span></span>

| <span data-ttu-id="e11c1-123">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e11c1-123">Location</span></span>      | <span data-ttu-id="e11c1-124">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="e11c1-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11c1-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="e11c1-125">GitHub</span></span>  | [<span data-ttu-id="e11c1-126">SearchFolder (ejemplo)</span><span class="sxs-lookup"><span data-stu-id="e11c1-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="e11c1-127">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e11c1-127">Building the Sample</span></span>

<span data-ttu-id="e11c1-128">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e11c1-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e11c1-129">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e11c1-129">Running the Sample</span></span>

<span data-ttu-id="e11c1-130">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e11c1-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



