---
description: A medida que las aplicaciones existentes se hacen obsoletas o ya no se usan, puede que tenga que quitarlas.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eliminar una aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423399"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="85022-103">Eliminar una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="85022-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="85022-104">A medida que las aplicaciones existentes se hacen obsoletas o ya no se usan, puede que tenga que quitarlas.</span><span class="sxs-lookup"><span data-stu-id="85022-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="85022-105">**Para eliminar una aplicación COM+**</span><span class="sxs-lookup"><span data-stu-id="85022-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="85022-106">En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo para el que desea eliminar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="85022-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="85022-107">Abra la carpeta **aplicaciones com+** del equipo especificado para mostrar todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="85022-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="85022-108">Seleccione la aplicación que desea quitar.</span><span class="sxs-lookup"><span data-stu-id="85022-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="85022-109">Si seleccionó una aplicación de servidor, cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="85022-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="85022-110">Para cerrar una aplicación, selecciónela en la herramienta administrativa Servicios de componentes, haga clic con el botón secundario y, a continuación, haga clic en **apagar**.</span><span class="sxs-lookup"><span data-stu-id="85022-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="85022-111">Si seleccionó una aplicación de biblioteca, asegúrese de que todos los procesos que usan actualmente esta aplicación de biblioteca están apagados.</span><span class="sxs-lookup"><span data-stu-id="85022-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="85022-112">En el menú **acción** , haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="85022-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="85022-113">También puede hacer clic con el botón secundario en el nombre de la aplicación y, a continuación, hacer clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="85022-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="85022-114">También puede eliminar una aplicación seleccionándola en la herramienta administrativa Servicios de componentes y presionando la tecla **Supr** , o bien puede seleccionar la aplicación, hacer clic con el botón secundario y, a continuación, hacer clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="85022-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="85022-115">Haga clic en **sí** cuando se le pida que confirme la acción.</span><span class="sxs-lookup"><span data-stu-id="85022-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="85022-116">Además, si una aplicación de servidor o proxy de aplicación se ha instalado en un equipo con Windows Installer (como se describe en "instalación de aplicaciones COM+" en la guía de administración de servicios de componentes), puede eliminarlo mediante la utilidad agregar o quitar programas del panel de control de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="85022-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="85022-117">O bien, puede eliminar un proxy de aplicación o aplicación de servidor instalado mediante el uso de la sintaxis de la línea de comandos de Windows Installer:</span><span class="sxs-lookup"><span data-stu-id="85022-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="85022-118">**msiexec-x nombre de** *aplicación \_ \* \* *. msi**</span><span class="sxs-lookup"><span data-stu-id="85022-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="85022-119">Estos métodos son especialmente útiles para eliminar aplicaciones COM+ en equipos cliente que no ejecuten la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="85022-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="85022-120">Al eliminar la aplicación, también se eliminan los componentes contenidos en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="85022-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="85022-121">Si estos componentes dependen de recursos adicionales (conexiones de bases de datos, archivos de datos o texto, configuración de raíz virtual de IIS, etc.), estos recursos se deben quitar a través de mecanismos distintos de la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="85022-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85022-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85022-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85022-123">Copiar componentes</span><span class="sxs-lookup"><span data-stu-id="85022-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="85022-124">Crear una nueva aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="85022-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="85022-125">Importar componentes</span><span class="sxs-lookup"><span data-stu-id="85022-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="85022-126">Instalación de nuevos componentes</span><span class="sxs-lookup"><span data-stu-id="85022-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="85022-127">Mover componentes</span><span class="sxs-lookup"><span data-stu-id="85022-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="85022-128">Quitar un componente de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="85022-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



