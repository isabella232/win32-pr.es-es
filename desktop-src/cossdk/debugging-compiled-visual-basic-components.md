---
description: Dado que en muchos casos podrá depurar solo una parte de la funcionalidad de los componentes dentro del entorno de Microsoft Visual Basic, habrá situaciones en las que necesitará depurar componentes compilados con Visual Basic una vez que se hayan compilado. Como el entorno de Visual Basic no lo habilita, en su lugar debe usar el entorno de Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Depurar componentes Visual Basic compilados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153066"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="06de8-104">Depurar componentes Visual Basic compilados</span><span class="sxs-lookup"><span data-stu-id="06de8-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="06de8-105">Dado que en muchos casos solo podrá depurar una parte de la funcionalidad del componente en el entorno de Microsoft Visual Basic, habrá situaciones en las que necesitará depurar los componentes compilados con Visual Basic una vez que se hayan compilado.</span><span class="sxs-lookup"><span data-stu-id="06de8-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="06de8-106">Como el entorno de Visual Basic no lo habilita, en su lugar debe usar el entorno de Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="06de8-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="06de8-107">**Para depurar un componente de Visual Basic en el entorno de Visual C++**</span><span class="sxs-lookup"><span data-stu-id="06de8-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="06de8-108">En Visual Basic 6,0, abra el proyecto de Visual Basic que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="06de8-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="06de8-109">En el menú **archivo** , haga clic en **crear YourProject.dll**.</span><span class="sxs-lookup"><span data-stu-id="06de8-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="06de8-110">En el cuadro de diálogo **crear proyecto** , haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="06de8-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="06de8-111">En el cuadro de diálogo **propiedades del proyecto** , en la pestaña **compilar** , haga clic en **compilar en código nativo** y **sin optimización** y seleccione la casilla **crear información de depuración simbólica** .</span><span class="sxs-lookup"><span data-stu-id="06de8-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="06de8-112">Haga clic en **Aceptar** y, a continuación, haga clic en **Aceptar** de nuevo para compilar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="06de8-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="06de8-113">Mueva la DLL compilada a la ubicación donde se instalan normalmente las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="06de8-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="06de8-114">Si no mueve el archivo DLL, es posible que reciba un mensaje de error que le informa de que no se pudo encontrar la información de depuración simbólica de la DLL.</span><span class="sxs-lookup"><span data-stu-id="06de8-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="06de8-115">Si tiene problemas para que el depurador se detenga en los puntos de interrupción del componente, confirme que el archivo DLL está en el directorio de paquetes estándar, elimine el componente de su paquete y vuelva a agregar el componente.</span><span class="sxs-lookup"><span data-stu-id="06de8-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="06de8-116">Inicie Visual C++.</span><span class="sxs-lookup"><span data-stu-id="06de8-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="06de8-117">En el menú **archivo** , haga clic en **abrir área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="06de8-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="06de8-118">En el cuadro de diálogo **abrir área de trabajo** , establezca **archivos de tipo** en **todos los archivos ( \* . \* )**, seleccione el componente compilado y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="06de8-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="06de8-119">En el menú **archivo** , haga clic en **abrir** (no **abrir área de trabajo**) y abra el módulo de Visual Basic (. Bas), el formulario (. FRM) o la clase (. CLS) que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="06de8-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="06de8-120">En el menú **proyecto** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="06de8-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="06de8-121">En el cuadro de diálogo **configuración del proyecto** , en la pestaña **depurar** , seleccione **General** en el cuadro **categoría** .</span><span class="sxs-lookup"><span data-stu-id="06de8-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="06de8-122">En el cuadro **ejecutable para sesión de depuración** , escriba la ruta de acceso completa de Dllhost.exe, seguido de un argumento que especifique el ID. de proceso de la aplicación com+ que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="06de8-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="06de8-123">Encontrará el identificador de proceso en la pestaña **General** del cuadro de diálogo **propiedades** de la aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="06de8-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="06de8-124">A continuación se encuentra un ejemplo: C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: { <processID> }.</span><span class="sxs-lookup"><span data-stu-id="06de8-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="06de8-125">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="06de8-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06de8-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06de8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06de8-127">Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS</span><span class="sxs-lookup"><span data-stu-id="06de8-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="06de8-128">Depuración en el IDE de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="06de8-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



