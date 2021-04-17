---
description: Para compilar aplicaciones de Tablet PC en C \# y Visual Basic .net, el proyecto en Microsoft Visual Studio .net debe incluir una referencia a los ensamblados de biblioteca administrada de Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca administrada y controles (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716716"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="f9b90-104">Biblioteca administrada y controles (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="f9b90-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="f9b90-105">Para compilar aplicaciones de Tablet PC en C \# y Visual Basic .net, el proyecto en Microsoft Visual Studio .net debe incluir una referencia a los ensamblados de biblioteca administrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f9b90-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="f9b90-106">Esto proporciona acceso al modelo de objetos administrados y a los controles.</span><span class="sxs-lookup"><span data-stu-id="f9b90-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="f9b90-107">Microsoft Visual C \# y visual Basic.net</span><span class="sxs-lookup"><span data-stu-id="f9b90-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="f9b90-108">En Windows Vista, los ensamblados de biblioteca administrada de Tablet PC se instalan de forma predeterminada en dos directorios:</span><span class="sxs-lookup"><span data-stu-id="f9b90-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="f9b90-109"><systemdrive>: Archivos de \\ programa archivos \\ comunes \\ Directorio de tinta compartida de Microsoft \\</span><span class="sxs-lookup"><span data-stu-id="f9b90-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="f9b90-110"><systemdrive>: \\ Archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="f9b90-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="f9b90-111">Para agregar una referencia a las bibliotecas administradas de la plataforma de Tablet PC en Microsoft Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="f9b90-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="f9b90-112">Abra el proyecto de Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="f9b90-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="f9b90-113">En el menú **Proyecto**, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="f9b90-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="f9b90-114">En la pestaña **.net** del cuadro de diálogo **Agregar referencia** , en la lista componentes, seleccione **Microsoft Tablet PC API**.</span><span class="sxs-lookup"><span data-stu-id="f9b90-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="f9b90-115">Haga clic en **seleccionar** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f9b90-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="f9b90-116">Para agregar una referencia a las API de análisis de tinta en Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="f9b90-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="f9b90-117">Abra el proyecto Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="f9b90-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="f9b90-118">En el menú **Proyecto**, haga clic en **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="f9b90-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="f9b90-119">En la pestaña **.net** del cuadro de diálogo **Agregar referencia** , en la lista componentes, seleccione **biblioteca administrada del análisis de tinta de Microsoft Tablet PC**.</span><span class="sxs-lookup"><span data-stu-id="f9b90-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="f9b90-120">Haga clic en **seleccionar** y, a continuación, en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f9b90-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="f9b90-121">Al compilar aplicaciones que usan Microsoft. Ink en Visual Studio 2005, debe seleccionar **proyecto**, seleccionar **propiedades**, seleccionar **compilar** y establecer destino de plataforma = x86.</span><span class="sxs-lookup"><span data-stu-id="f9b90-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="f9b90-122">Esta opción no está disponible en Microsoft Visual Studio Express productos.</span><span class="sxs-lookup"><span data-stu-id="f9b90-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



