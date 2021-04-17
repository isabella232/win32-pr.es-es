---
description: Utilice el procedimiento siguiente para depurar a los expertos escritos en Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Depuración de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667734"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="9cc5b-103">Depuración de un experto</span><span class="sxs-lookup"><span data-stu-id="9cc5b-103">Debugging an Expert</span></span>

<span data-ttu-id="9cc5b-104">Utilice el procedimiento siguiente para depurar a los expertos escritos en Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="9cc5b-105">**Depuración de un experto**</span><span class="sxs-lookup"><span data-stu-id="9cc5b-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="9cc5b-106">Instale el experto (archivo DLL) y el archivo de base de datos de programa (. pdb) que se genera al compilar el experto en la ubicación correcta.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="9cc5b-107">Para obtener más información, consulte [instalación de un experto en Monitor de red 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="9cc5b-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="9cc5b-108">Inicie Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="9cc5b-109">En el menú **archivo** , haga clic en **abrir** y seleccione el nombre de la dll experta.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="9cc5b-110">Después de cargar Microsoft Visual C++, haga clic en el menú **proyecto** y, a continuación, en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="9cc5b-111">Haga clic en **depurar**.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-111">Click **Debug**.</span></span> <span data-ttu-id="9cc5b-112">En **ejecutable para sesión de depuración**, escriba la ruta de acceso completa de Netmon.exe, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9cc5b-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="9cc5b-113">Establezca los puntos de interrupción en el código.</span><span class="sxs-lookup"><span data-stu-id="9cc5b-113">Set the breakpoints in your code.</span></span>

 

 



