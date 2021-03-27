---
description: Muestra cómo utilizar la interfaz IShellLibrary para crear una aplicación de línea de comandos que proporciona acceso mediante programación para inspeccionar y manipular archivos de biblioteca y bibliotecas.
title: Ejemplo de línea de comandos de biblioteca de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5EC06E69-8AC8-4d9e-BAFC-C1AFC1294023
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9db182498791fee344061c91ea570ed770f3a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498082"
---
# <a name="shell-library-command-line-sample"></a><span data-ttu-id="c6cd2-103">Ejemplo de línea de comandos de biblioteca de shell</span><span class="sxs-lookup"><span data-stu-id="c6cd2-103">Shell Library Command Line Sample</span></span>

<span data-ttu-id="c6cd2-104">Muestra cómo utilizar la interfaz [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para crear una aplicación de línea de comandos que proporciona acceso mediante programación para inspeccionar y manipular archivos de biblioteca y bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="c6cd2-104">Demonstrates how to use the [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) interface to create a command-line application that provides programmatic access for inspecting and manipulating libraries and library files.</span></span>

<span data-ttu-id="c6cd2-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="c6cd2-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c6cd2-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6cd2-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c6cd2-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cd2-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c6cd2-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cd2-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c6cd2-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cd2-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="c6cd2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6cd2-110">Requirements</span></span>



| <span data-ttu-id="c6cd2-111">Producto</span><span class="sxs-lookup"><span data-stu-id="c6cd2-111">Product</span></span>                                | <span data-ttu-id="c6cd2-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="c6cd2-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c6cd2-113">Windows</span><span class="sxs-lookup"><span data-stu-id="c6cd2-113">Windows</span></span>                                | <span data-ttu-id="c6cd2-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6cd2-114">Windows 7</span></span>               |
| <span data-ttu-id="c6cd2-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="c6cd2-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c6cd2-116">7.0</span><span class="sxs-lookup"><span data-stu-id="c6cd2-116">7.0</span></span>                     |



 

<span data-ttu-id="c6cd2-117">Para conocer los requisitos adicionales, consulte el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c6cd2-117">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c6cd2-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cd2-118">Downloading the Sample</span></span>

| <span data-ttu-id="c6cd2-119">Ubicación</span><span class="sxs-lookup"><span data-stu-id="c6cd2-119">Location</span></span>      | <span data-ttu-id="c6cd2-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="c6cd2-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6cd2-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="c6cd2-121">GitHub</span></span>  | [<span data-ttu-id="c6cd2-122">Ejemplo de ShellLibraryCommandLine</span><span class="sxs-lookup"><span data-stu-id="c6cd2-122">ShellLibraryCommandLine sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryCommandLine) |

## <a name="building-the-sample"></a><span data-ttu-id="c6cd2-123">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cd2-123">Building the Sample</span></span>

<span data-ttu-id="c6cd2-124">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c6cd2-124">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c6cd2-125">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cd2-125">Running the Sample</span></span>

<span data-ttu-id="c6cd2-126">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c6cd2-126">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



