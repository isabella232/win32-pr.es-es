---
title: Ejemplo de VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Más información acerca de: ejemplo VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659669"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="4e5ac-103">Ejemplo de VListVW</span><span class="sxs-lookup"><span data-stu-id="4e5ac-103">VListVW Sample</span></span>

<span data-ttu-id="4e5ac-104">En este tema se describe el ejemplo de código de ejemplo VListVW.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="4e5ac-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e5ac-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="4e5ac-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e5ac-106">Description</span></span>](#description)
-   [<span data-ttu-id="4e5ac-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="4e5ac-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="4e5ac-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e5ac-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4e5ac-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e5ac-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4e5ac-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e5ac-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="4e5ac-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e5ac-111">Description</span></span>

<span data-ttu-id="4e5ac-112">En el ejemplo VListVW se muestra cómo implementar un control de vista de lista virtual simple en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="4e5ac-113">Un control de vista de lista virtual es un control de vista de lista estándar con el estilo **LVS \_ OWNERDATA** .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="4e5ac-114">En este ejemplo se crea un control de vista de lista que "prácticamente" contiene 100.000 elementos.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="4e5ac-115">Los elementos nunca se agregan realmente.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-115">The items are never actually added.</span></span> <span data-ttu-id="4e5ac-116">En su lugar, el control de vista de lista virtual se "indica" el número de elementos que contiene con el mensaje [**\_ SETITEMCOUNT de LVM**](lvm-setitemcount.md) .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="4e5ac-117">Cuando es necesario dibujar un elemento, el control de vista de lista consulta la información de presentación de la ventana primaria con la notificación [ \_ GETDISPINFO de LVN](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="4e5ac-118">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="4e5ac-118">Minimum Requirements</span></span>



| <span data-ttu-id="4e5ac-119">Producto</span><span class="sxs-lookup"><span data-stu-id="4e5ac-119">Product</span></span>          | <span data-ttu-id="4e5ac-120">Versión</span><span class="sxs-lookup"><span data-stu-id="4e5ac-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="4e5ac-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e5ac-121">DLL</span></span>              | <span data-ttu-id="4e5ac-122">comctl32.dll versión 4,70</span><span class="sxs-lookup"><span data-stu-id="4e5ac-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="4e5ac-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="4e5ac-123">Operating System</span></span> | <span data-ttu-id="4e5ac-124">Windows 95, Microsoft Windows NT 3,51</span><span class="sxs-lookup"><span data-stu-id="4e5ac-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4e5ac-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e5ac-125">Downloading the Sample</span></span>

<span data-ttu-id="4e5ac-126">El ejemplo VListVW está disponible en github en el [repositorio de ejemplos de Windows clásico](https://github.com/microsoft/Windows-classic-samples).</span><span class="sxs-lookup"><span data-stu-id="4e5ac-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="4e5ac-127">Los ejemplos de elementos de control de vista de lista se pueden encontrar [aquí](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw) .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="4e5ac-128">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e5ac-128">Building the Sample</span></span>

<span data-ttu-id="4e5ac-129">Para compilar el ejemplo mediante el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="4e5ac-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="4e5ac-130">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="4e5ac-131">Escriba `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="4e5ac-132">Para compilar el ejemplo con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="4e5ac-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="4e5ac-133">Abra el explorador de Windows y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="4e5ac-134">Haga doble clic en el icono del archivo. vcproj para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="4e5ac-135">En el menú **compilar** , seleccione **compilar solución** para compilar la solución.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e5ac-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e5ac-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e5ac-137">Acerca de los controles List-View</span><span class="sxs-lookup"><span data-stu-id="4e5ac-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




