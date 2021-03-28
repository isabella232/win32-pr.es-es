---
description: Para agregar un elemento al submenú programas, siga estos pasos.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Cómo agregar accesos directos al menú Inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156476"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="e7604-103">Cómo agregar accesos directos al menú Inicio</span><span class="sxs-lookup"><span data-stu-id="e7604-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="e7604-104">Para agregar un elemento al submenú **programas** , siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="e7604-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="e7604-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e7604-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e7604-106">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="e7604-106">Step 1:</span></span>

<span data-ttu-id="e7604-107">Cree un [vínculo de Shell](./links.md) mediante la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="e7604-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="e7604-108">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="e7604-108">Step 2:</span></span>

<span data-ttu-id="e7604-109">Obtenga la ubicación de la carpeta programas mediante la función [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , pasando [**FOLDERID \_ programas**](knownfolderid.md).</span><span class="sxs-lookup"><span data-stu-id="e7604-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="e7604-110">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="e7604-110">Step 3:</span></span>

<span data-ttu-id="e7604-111">Agregue el vínculo de Shell a la carpeta programas.</span><span class="sxs-lookup"><span data-stu-id="e7604-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="e7604-112">También puede crear una carpeta en la carpeta programas y agregar el vínculo a esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="e7604-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
