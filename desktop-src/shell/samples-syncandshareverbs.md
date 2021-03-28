---
description: Muestra cómo registrar un verbo que extiende el &\# 0034; Sincronizar&\# 0034 y &\# 0034; Compartir&\# 0034; verbos en la barra de comandos del explorador de Windows.
title: Verbos Sincronizar y Compartir
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986035"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="dc298-103">Verbos Sincronizar y Compartir</span><span class="sxs-lookup"><span data-stu-id="dc298-103">Sync and Share Verbs</span></span>

<span data-ttu-id="dc298-104">Muestra cómo registrar un verbo que extiende los verbos "sincronizar" y "compartir" en la barra de comandos del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc298-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="dc298-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="dc298-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dc298-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc298-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="dc298-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc298-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="dc298-108">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc298-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="dc298-109">Quitar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc298-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="dc298-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc298-110">Requirements</span></span>



| <span data-ttu-id="dc298-111">Producto</span><span class="sxs-lookup"><span data-stu-id="dc298-111">Product</span></span>                                | <span data-ttu-id="dc298-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="dc298-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="dc298-113">Windows</span><span class="sxs-lookup"><span data-stu-id="dc298-113">Windows</span></span>                                | <span data-ttu-id="dc298-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dc298-114">Windows 7</span></span>               |
| <span data-ttu-id="dc298-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="dc298-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="dc298-116">7.0</span><span class="sxs-lookup"><span data-stu-id="dc298-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="dc298-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc298-117">Downloading the Sample</span></span>

| <span data-ttu-id="dc298-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="dc298-118">Location</span></span>      | <span data-ttu-id="dc298-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="dc298-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc298-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="dc298-120">GitHub</span></span>  | [<span data-ttu-id="dc298-121">Ejemplo de SyncAndShareVerbs</span><span class="sxs-lookup"><span data-stu-id="dc298-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="dc298-122">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc298-122">Running the Sample</span></span>

<span data-ttu-id="dc298-123">Para ejecutar el ejemplo (Sync):</span><span class="sxs-lookup"><span data-stu-id="dc298-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="dc298-124">Navegue hasta el directorio que contiene el `sync.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="dc298-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="dc298-125">Escriba `sync.reg ` en la línea de comandos o haga doble clic en el icono `sync.reg` registrarlo.</span><span class="sxs-lookup"><span data-stu-id="dc298-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="dc298-126">Abra el explorador de Windows y seleccione un archivo.</span><span class="sxs-lookup"><span data-stu-id="dc298-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="dc298-127">Haga clic en la opción **sincronizar** en la barra de comandos y seleccione una subopción como **Paint**.</span><span class="sxs-lookup"><span data-stu-id="dc298-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="dc298-128">Para ejecutar el ejemplo (recurso compartido):</span><span class="sxs-lookup"><span data-stu-id="dc298-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="dc298-129">Navegue hasta el directorio que contiene el `share.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="dc298-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="dc298-130">Escriba `share.reg` en la línea de comandos o haga doble clic en el icono `share.reg` registrarlo.</span><span class="sxs-lookup"><span data-stu-id="dc298-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="dc298-131">Abra el explorador de Windows y seleccione un archivo.</span><span class="sxs-lookup"><span data-stu-id="dc298-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="dc298-132">Haga clic en la opción **compartir** en la barra de comandos.</span><span class="sxs-lookup"><span data-stu-id="dc298-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="dc298-133">Haga clic en la opción **compartir con** en la barra de comandos y seleccione una subopción como **Paint**.</span><span class="sxs-lookup"><span data-stu-id="dc298-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="dc298-134">Quitar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc298-134">Removing the Sample</span></span>

<span data-ttu-id="dc298-135">Para quitar el ejemplo (Sync):</span><span class="sxs-lookup"><span data-stu-id="dc298-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="dc298-136">Navegue hasta el directorio que contiene el archivo Uninstallsync. reg.</span><span class="sxs-lookup"><span data-stu-id="dc298-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="dc298-137">Escriba `uninstallsync.reg` en la línea de comandos o haga doble clic en el icono de `uninstallsync.reg` .</span><span class="sxs-lookup"><span data-stu-id="dc298-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="dc298-138">Para quitar el ejemplo (recurso compartido):</span><span class="sxs-lookup"><span data-stu-id="dc298-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="dc298-139">Navegue hasta el directorio que contiene el archivo Uninstallshare. reg.</span><span class="sxs-lookup"><span data-stu-id="dc298-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="dc298-140">Escriba `uninstallshare.reg` en la línea de comandos o haga doble clic en el icono de `uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="dc298-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



