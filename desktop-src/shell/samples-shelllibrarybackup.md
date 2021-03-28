---
description: Muestra cómo enumerar las bibliotecas como contenedores.
title: Ejemplo de copia de seguridad de biblioteca de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986039"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="e4d32-103">Ejemplo de copia de seguridad de biblioteca de shell</span><span class="sxs-lookup"><span data-stu-id="e4d32-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="e4d32-104">Muestra cómo enumerar las bibliotecas como contenedores.</span><span class="sxs-lookup"><span data-stu-id="e4d32-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="e4d32-105">Las bibliotecas son el nuevo paradigma de almacenamiento para los archivos de usuario y se introducen en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4d32-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="e4d32-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="e4d32-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e4d32-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4d32-107">Description</span></span>](#description)
-   [<span data-ttu-id="e4d32-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4d32-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e4d32-109">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4d32-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e4d32-110">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4d32-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="e4d32-111">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4d32-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="e4d32-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4d32-112">Description</span></span>

<span data-ttu-id="e4d32-113">Este ejemplo es una aplicación de copia de seguridad ficticia que muestra cómo elegir bibliotecas a través del cuadro de diálogo archivo común.</span><span class="sxs-lookup"><span data-stu-id="e4d32-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="e4d32-114">También muestra cómo realizar copias de seguridad de las bibliotecas mediante el rastreador de espacios de nombres de Shell.</span><span class="sxs-lookup"><span data-stu-id="e4d32-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d32-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4d32-115">Requirements</span></span>



| <span data-ttu-id="e4d32-116">Producto</span><span class="sxs-lookup"><span data-stu-id="e4d32-116">Product</span></span>                                | <span data-ttu-id="e4d32-117">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="e4d32-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e4d32-118">Windows</span><span class="sxs-lookup"><span data-stu-id="e4d32-118">Windows</span></span>                                | <span data-ttu-id="e4d32-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d32-119">Windows 7</span></span>               |
| <span data-ttu-id="e4d32-120">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="e4d32-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e4d32-121">7.0</span><span class="sxs-lookup"><span data-stu-id="e4d32-121">7.0</span></span>                     |



 

<span data-ttu-id="e4d32-122">Para conocer los requisitos adicionales, consulte el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4d32-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="e4d32-123">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4d32-123">Downloading the Sample</span></span>

| <span data-ttu-id="e4d32-124">Ubicación</span><span class="sxs-lookup"><span data-stu-id="e4d32-124">Location</span></span>      | <span data-ttu-id="e4d32-125">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="e4d32-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d32-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="e4d32-126">GitHub</span></span>  | [<span data-ttu-id="e4d32-127">Ejemplo de ShellLibraryBackup</span><span class="sxs-lookup"><span data-stu-id="e4d32-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="e4d32-128">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4d32-128">Building the Sample</span></span>

<span data-ttu-id="e4d32-129">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4d32-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e4d32-130">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4d32-130">Running the Sample</span></span>

<span data-ttu-id="e4d32-131">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4d32-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



