---
description: Muestra cómo llamar a la función ShellExecute desde el proceso del explorador de Windows.
title: Ejemplo de ejecución en Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D307B22A-E4A3-4215-B28E-F48A721260A1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7a511f7ccc7edd218edd405de163501afd530f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985586"
---
# <a name="execute-in-explorer-sample"></a><span data-ttu-id="3aa5b-103">Ejemplo de ejecución en Explorer</span><span class="sxs-lookup"><span data-stu-id="3aa5b-103">Execute In Explorer Sample</span></span>

<span data-ttu-id="3aa5b-104">Muestra cómo llamar a la función [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) desde el proceso del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa5b-104">Demonstrates how to call the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function from the Windows Explorer process.</span></span> <span data-ttu-id="3aa5b-105">Esto resulta útil cuando se inicia un proceso sin privilegios desde un proceso con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="3aa5b-105">This is useful when launching an unelevated process from an elevated process.</span></span>

<span data-ttu-id="3aa5b-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="3aa5b-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3aa5b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa5b-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3aa5b-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aa5b-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3aa5b-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aa5b-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3aa5b-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aa5b-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="3aa5b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa5b-111">Requirements</span></span>



| <span data-ttu-id="3aa5b-112">Producto</span><span class="sxs-lookup"><span data-stu-id="3aa5b-112">Product</span></span>                                | <span data-ttu-id="3aa5b-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="3aa5b-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3aa5b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="3aa5b-114">Windows</span></span>                                | <span data-ttu-id="3aa5b-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3aa5b-115">Windows Vista</span></span>           |
| <span data-ttu-id="3aa5b-116">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="3aa5b-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3aa5b-117">7.0</span><span class="sxs-lookup"><span data-stu-id="3aa5b-117">7.0</span></span>                     |



 

<span data-ttu-id="3aa5b-118">Para conocer los requisitos adicionales, consulte el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3aa5b-118">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3aa5b-119">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aa5b-119">Downloading the Sample</span></span>

| <span data-ttu-id="3aa5b-120">Ubicación</span><span class="sxs-lookup"><span data-stu-id="3aa5b-120">Location</span></span>      | <span data-ttu-id="3aa5b-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="3aa5b-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa5b-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="3aa5b-122">GitHub</span></span>  | [<span data-ttu-id="3aa5b-123">Ejemplo de ExecInExplorer</span><span class="sxs-lookup"><span data-stu-id="3aa5b-123">ExecInExplorer sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ExecInExplorer) |

## <a name="building-the-sample"></a><span data-ttu-id="3aa5b-124">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aa5b-124">Building the Sample</span></span>

<span data-ttu-id="3aa5b-125">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3aa5b-125">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3aa5b-126">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aa5b-126">Running the Sample</span></span>

<span data-ttu-id="3aa5b-127">Para obtener instrucciones sobre cómo generar el ejemplo, vea el archivo Léame incluido con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3aa5b-127">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



