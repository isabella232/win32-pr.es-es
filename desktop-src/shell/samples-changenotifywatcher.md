---
description: Muestra cómo escuchar las notificaciones de cambios de Shell en una carpeta o un elemento en el espacio de nombres del explorador de Windows.
title: Ejemplo de cambio del monitor de notificaciones
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278014"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="0f3c1-103">Ejemplo de cambio del monitor de notificaciones</span><span class="sxs-lookup"><span data-stu-id="0f3c1-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="0f3c1-104">Muestra cómo escuchar las notificaciones de cambios de Shell en una carpeta o un elemento en el espacio de nombres del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="0f3c1-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0f3c1-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f3c1-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0f3c1-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f3c1-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0f3c1-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f3c1-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0f3c1-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f3c1-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="0f3c1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f3c1-110">Requirements</span></span>



| <span data-ttu-id="0f3c1-111">Producto</span><span class="sxs-lookup"><span data-stu-id="0f3c1-111">Product</span></span>                                | <span data-ttu-id="0f3c1-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="0f3c1-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="0f3c1-113">Windows</span><span class="sxs-lookup"><span data-stu-id="0f3c1-113">Windows</span></span>                                | <span data-ttu-id="0f3c1-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f3c1-114">Windows Vista</span></span>           |
| <span data-ttu-id="0f3c1-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="0f3c1-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="0f3c1-116">7.0</span><span class="sxs-lookup"><span data-stu-id="0f3c1-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0f3c1-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f3c1-117">Downloading the Sample</span></span>

| <span data-ttu-id="0f3c1-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="0f3c1-118">Location</span></span>      | <span data-ttu-id="0f3c1-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="0f3c1-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3c1-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="0f3c1-120">GitHub</span></span>  | [<span data-ttu-id="0f3c1-121">Ejemplo de ChangeNotifyWatcher</span><span class="sxs-lookup"><span data-stu-id="0f3c1-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="0f3c1-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f3c1-122">Building the Sample</span></span>

<span data-ttu-id="0f3c1-123">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="0f3c1-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="0f3c1-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="0f3c1-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="0f3c1-125">Escriba `msbuild ChangeNotifyWatcher.sln`.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="0f3c1-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="0f3c1-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0f3c1-127">Abra el explorador de Windows y navegue hasta el directorio del proyecto **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="0f3c1-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="0f3c1-128">Haga doble clic en el icono del archivo ChangeNotifyWatcher. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="0f3c1-129">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0f3c1-130">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f3c1-130">Running the Sample</span></span>

1.  <span data-ttu-id="0f3c1-131">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="0f3c1-132">En el símbolo del sistema, escriba `ChangeNotifyWatcher.exe`.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="0f3c1-133">Como alternativa, en el explorador de Windows, haga doble clic en el icono de ChangeNotifyWatcher.exe.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="0f3c1-134">Para demostrar el efecto, los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) seleccionan la carpeta que se va a ver haciendo clic en **"Pick..."** o mediante arrastrar y colocar en una carpeta de una ventana del explorador de Windows en la vista de lista del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0f3c1-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 



