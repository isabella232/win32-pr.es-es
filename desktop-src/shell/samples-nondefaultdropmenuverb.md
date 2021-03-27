---
description: Muestra cómo extender el menú contextual de arrastrar y colocar (a veces conocido como menú contextual).
title: Ejemplo de NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361185"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="d68b5-103">Ejemplo de NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="d68b5-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="d68b5-104">Muestra cómo extender el menú contextual de arrastrar y colocar (a veces conocido como menú contextual).</span><span class="sxs-lookup"><span data-stu-id="d68b5-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="d68b5-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="d68b5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d68b5-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d68b5-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d68b5-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b5-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d68b5-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b5-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d68b5-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b5-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="d68b5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d68b5-110">Requirements</span></span>



| <span data-ttu-id="d68b5-111">Producto</span><span class="sxs-lookup"><span data-stu-id="d68b5-111">Product</span></span>                                | <span data-ttu-id="d68b5-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="d68b5-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d68b5-113">Windows</span><span class="sxs-lookup"><span data-stu-id="d68b5-113">Windows</span></span>                                | <span data-ttu-id="d68b5-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d68b5-114">Windows Vista</span></span>           |
| <span data-ttu-id="d68b5-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="d68b5-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d68b5-116">7.0</span><span class="sxs-lookup"><span data-stu-id="d68b5-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d68b5-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b5-117">Downloading the Sample</span></span>

| <span data-ttu-id="d68b5-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="d68b5-118">Location</span></span>      | <span data-ttu-id="d68b5-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d68b5-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68b5-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="d68b5-120">GitHub</span></span>  | [<span data-ttu-id="d68b5-121">Ejemplo de NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="d68b5-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="d68b5-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b5-122">Building the Sample</span></span>

<span data-ttu-id="d68b5-123">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="d68b5-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d68b5-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="d68b5-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="d68b5-125">Escriba `msbuild NonDefaultDropMenuVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="d68b5-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="d68b5-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="d68b5-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="d68b5-127">Abra el explorador de Windows y navegue hasta el directorio del proyecto **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="d68b5-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="d68b5-128">Haga doble clic en el icono del archivo NonDefaultDropMenuVerb. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d68b5-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d68b5-129">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="d68b5-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d68b5-130">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b5-130">Running the Sample</span></span>

1.  <span data-ttu-id="d68b5-131">Navegue hasta el directorio que contiene el nuevo archivo DLL mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="d68b5-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="d68b5-132">Copie NonDefaultDropMenuVerb.dll en el directorio del sistema (por ejemplo, C: \\ Windows \\ system32).</span><span class="sxs-lookup"><span data-stu-id="d68b5-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="d68b5-133">En un símbolo del sistema, escriba `regedit NonDefaultDropMenuVerb.reg` .</span><span class="sxs-lookup"><span data-stu-id="d68b5-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="d68b5-134">Use el botón secundario del mouse para arrastrar un archivo de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="d68b5-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="d68b5-135">Verá elementos de menú adicionales para la operación de colocar.</span><span class="sxs-lookup"><span data-stu-id="d68b5-135">You will see additional menu items for the drop operation.</span></span>

 

 



