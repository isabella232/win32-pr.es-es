---
description: Módulos de TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Módulos de TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082433"
---
# <a name="topoedit-modules"></a><span data-ttu-id="bd2fc-103">Módulos de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bd2fc-103">TopoEdit Modules</span></span>

<span data-ttu-id="bd2fc-104">La herramienta TopoEdit se proporciona con el Windows SDK para Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bd2fc-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="bd2fc-105">La herramienta requiere Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="bd2fc-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="bd2fc-106">Los módulos TopoEdit se encuentran en la carpeta bin del SDK de.</span><span class="sxs-lookup"><span data-stu-id="bd2fc-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="bd2fc-107">Estos módulos son:</span><span class="sxs-lookup"><span data-stu-id="bd2fc-107">These modules are:</span></span>

-   <span data-ttu-id="bd2fc-108">TopoEdit.exe: ejecutable de la aplicación</span><span class="sxs-lookup"><span data-stu-id="bd2fc-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="bd2fc-109">TEDUTIL.dll: DLL de extensión</span><span class="sxs-lookup"><span data-stu-id="bd2fc-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="bd2fc-110">La instalación del SDK registra el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="bd2fc-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="bd2fc-111">Sin embargo, si se produce un error, en un símbolo del sistema, ejecute lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="bd2fc-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="bd2fc-112">El código fuente de TopoEdit también se proporciona como un ejemplo en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bd2fc-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="bd2fc-113">Se encuentra en el siguiente directorio:</span><span class="sxs-lookup"><span data-stu-id="bd2fc-113">It is located in the following directory:</span></span>

<span data-ttu-id="bd2fc-114"><samples root>\\Multimedia \\ Media Foundation \\ TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bd2fc-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd2fc-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd2fc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd2fc-116">Introducción a TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bd2fc-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="bd2fc-117">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bd2fc-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



