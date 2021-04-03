---
title: Ejemplo de rebar
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: 'Más información sobre: ejemplo rebar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998119"
---
# <a name="rebar-sample"></a><span data-ttu-id="2cc03-103">Ejemplo de rebar</span><span class="sxs-lookup"><span data-stu-id="2cc03-103">Rebar Sample</span></span>

<span data-ttu-id="2cc03-104">En este tema se describe el ejemplo de código de ejemplo rebar.</span><span class="sxs-lookup"><span data-stu-id="2cc03-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="2cc03-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2cc03-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="2cc03-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cc03-106">Description</span></span>](#description)
-   [<span data-ttu-id="2cc03-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="2cc03-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="2cc03-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc03-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2cc03-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc03-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2cc03-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cc03-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="2cc03-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cc03-111">Description</span></span>

<span data-ttu-id="2cc03-112">El ejemplo rebar muestra cómo implementar un control común rebar simple en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cc03-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="2cc03-113">En este ejemplo se crea un control rebar que tiene dos bandas.</span><span class="sxs-lookup"><span data-stu-id="2cc03-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="2cc03-114">Una contiene un cuadro combinado y el otro contiene un botón de reenvío.</span><span class="sxs-lookup"><span data-stu-id="2cc03-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="2cc03-115">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="2cc03-115">Minimum Requirements</span></span>



| <span data-ttu-id="2cc03-116">Producto</span><span class="sxs-lookup"><span data-stu-id="2cc03-116">Product</span></span>          | <span data-ttu-id="2cc03-117">Versión</span><span class="sxs-lookup"><span data-stu-id="2cc03-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="2cc03-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cc03-118">DLL</span></span>              | <span data-ttu-id="2cc03-119">comctl32.dll versión 4,71</span><span class="sxs-lookup"><span data-stu-id="2cc03-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="2cc03-120">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2cc03-120">Operating System</span></span> | <span data-ttu-id="2cc03-121">Windows 95 con Internet Explorer 4,0</span><span class="sxs-lookup"><span data-stu-id="2cc03-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2cc03-122">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc03-122">Downloading the Sample</span></span>

<span data-ttu-id="2cc03-123">El ejemplo rebar se instala como parte del [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx) y está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="2cc03-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="2cc03-124">Location</span><span class="sxs-lookup"><span data-stu-id="2cc03-124">Location</span></span>    | <span data-ttu-id="2cc03-125">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="2cc03-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc03-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2cc03-126">Windows SDK</span></span> | <span data-ttu-id="2cc03-127">% Archivos de programa% \\ Microsoft SDK \\ Windows número de versión de \\ \[ \] \\ ejemplo \\ WinUI \\ Controls \\ Common \\ rebar</span><span class="sxs-lookup"><span data-stu-id="2cc03-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="2cc03-128">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc03-128">Building the Sample</span></span>

<span data-ttu-id="2cc03-129">Para compilar el ejemplo mediante el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="2cc03-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="2cc03-130">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="2cc03-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="2cc03-131">Escriba `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="2cc03-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="2cc03-132">Para compilar el ejemplo con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="2cc03-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="2cc03-133">Abra el explorador de Windows y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="2cc03-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="2cc03-134">Haga doble clic en el icono del archivo. vcproj para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2cc03-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="2cc03-135">En el menú **compilar** , seleccione **compilar solución** para compilar la solución.</span><span class="sxs-lookup"><span data-stu-id="2cc03-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cc03-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cc03-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cc03-137">Rebar (controles)</span><span class="sxs-lookup"><span data-stu-id="2cc03-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




