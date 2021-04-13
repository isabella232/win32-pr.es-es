---
description: En el ejemplo de código WSFromScript se muestra cómo consultar Windows Search desde un script de Microsoft Visual Basic mediante Microsoft Objetos de datos ActiveX (ADO).
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: WSFromScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360193"
---
# <a name="wsfromscript"></a><span data-ttu-id="f6f20-103">WSFromScript</span><span class="sxs-lookup"><span data-stu-id="f6f20-103">WSFromScript</span></span>

<span data-ttu-id="f6f20-104">En el ejemplo de código WSFromScript se muestra cómo consultar Windows Search desde un script de Microsoft Visual Basic mediante Microsoft Objetos de datos ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="f6f20-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="f6f20-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f6f20-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="f6f20-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f20-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="f6f20-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6f20-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="f6f20-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6f20-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="f6f20-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6f20-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="f6f20-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f20-110">Requirements</span></span>

| <span data-ttu-id="f6f20-111">Producto</span><span class="sxs-lookup"><span data-stu-id="f6f20-111">Product</span></span>     | <span data-ttu-id="f6f20-112">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="f6f20-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="f6f20-113">Windows</span><span class="sxs-lookup"><span data-stu-id="f6f20-113">Windows</span></span>     | <span data-ttu-id="f6f20-114">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="f6f20-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="f6f20-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f6f20-115">Windows SDK</span></span> | <span data-ttu-id="f6f20-116">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="f6f20-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="f6f20-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6f20-117">Downloading the Sample</span></span>

<span data-ttu-id="f6f20-118">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="f6f20-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="f6f20-119">Location</span><span class="sxs-lookup"><span data-stu-id="f6f20-119">Location</span></span>      | <span data-ttu-id="f6f20-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="f6f20-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f6f20-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="f6f20-121">GitHub</span></span>  | [<span data-ttu-id="f6f20-122">Ejemplo de WSFromScript</span><span class="sxs-lookup"><span data-stu-id="f6f20-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="f6f20-123">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="f6f20-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="f6f20-124">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6f20-124">Building the Sample</span></span>

<span data-ttu-id="f6f20-125">Para compilar el ejemplo desde la ventana del símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="f6f20-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="f6f20-126">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **QueryEverything** .</span><span class="sxs-lookup"><span data-stu-id="f6f20-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="f6f20-127">Por ejemplo, la ruta de instalación predeterminada completa del SDK de Windows 7 es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` .</span><span class="sxs-lookup"><span data-stu-id="f6f20-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="f6f20-128">Escriba `cscript QueryEverything.vbs`.</span><span class="sxs-lookup"><span data-stu-id="f6f20-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6f20-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6f20-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="f6f20-130">Conceptual</span><span class="sxs-lookup"><span data-stu-id="f6f20-130">Conceptual</span></span>

<span data-ttu-id="f6f20-131">[**Referencia del lenguaje VBScript**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="f6f20-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="f6f20-132">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6f20-132">Other Samples</span></span>

[<span data-ttu-id="f6f20-133">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="f6f20-133">Search Code Samples</span></span>](-search-samples-ovw.md)
