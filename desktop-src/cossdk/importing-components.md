---
description: Puede usar la herramienta administrativa Servicios de componentes para importar en componentes específicos de aplicaciones que ya se han registrado en el equipo como componentes COM en el registro de Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496030"
---
# <a name="importing-components"></a><span data-ttu-id="a61ca-103">Importar componentes</span><span class="sxs-lookup"><span data-stu-id="a61ca-103">Importing Components</span></span>

<span data-ttu-id="a61ca-104">Puede usar la herramienta administrativa Servicios de componentes para importar en componentes específicos de aplicaciones que ya se han registrado en el equipo como componentes COM en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="a61ca-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="a61ca-105">Al importar un componente, no se instala la interfaz o la información de método necesaria para establecer las propiedades de la interfaz o para configurar el acceso al componente desde un cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="a61ca-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="a61ca-106">Por lo tanto, si es posible, debe instalar en lugar de importar componentes sin configurar.</span><span class="sxs-lookup"><span data-stu-id="a61ca-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="a61ca-107">Al importar un componente en una aplicación COM+, COM+ no rellena la información de interfaz y de método para el componente.</span><span class="sxs-lookup"><span data-stu-id="a61ca-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="a61ca-108">Durante la exportación de un proxy de aplicación, COM+ no proporcionará información de serialización (bibliotecas de tipos o proxy/código auxiliar) para algunas o todas las interfaces.</span><span class="sxs-lookup"><span data-stu-id="a61ca-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="a61ca-109">Se producirá un error en la exportación de proxies de aplicación que contienen componentes importados o se producirá una advertencia.</span><span class="sxs-lookup"><span data-stu-id="a61ca-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="a61ca-110">**Para importar un componente en una aplicación COM+**</span><span class="sxs-lookup"><span data-stu-id="a61ca-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="a61ca-111">En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo que hospeda la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="a61ca-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="a61ca-112">Abra la carpeta **aplicaciones com+** para ese equipo y seleccione la aplicación en la que desea instalar el componente.</span><span class="sxs-lookup"><span data-stu-id="a61ca-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="a61ca-113">Abra la carpeta de la aplicación y seleccione **componentes**.</span><span class="sxs-lookup"><span data-stu-id="a61ca-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="a61ca-114">En el menú **acción** , seleccione **nuevo** y, a continuación, haga clic en **componente**.</span><span class="sxs-lookup"><span data-stu-id="a61ca-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="a61ca-115">También puede hacer clic con el botón secundario en la carpeta **componentes** , seleccionar **nuevo** y, a continuación, hacer clic en **componente**.</span><span class="sxs-lookup"><span data-stu-id="a61ca-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="a61ca-116">En la página **principal** del Asistente para instalación de aplicaciones com+, haga clic en **siguiente** y, en el cuadro de diálogo **importar o instalar un componente** , haga clic en **importar componentes que ya están registrados**.</span><span class="sxs-lookup"><span data-stu-id="a61ca-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="a61ca-117">En el cuadro de diálogo **elegir los componentes que se van a importar** , active la casilla **detalles** para ver información completa sobre los componentes que ya están registrados.</span><span class="sxs-lookup"><span data-stu-id="a61ca-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="a61ca-118">Seleccione los componentes que desea importar en la lista que aparece y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a61ca-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="a61ca-119">Haga clic en **Finalizar**</span><span class="sxs-lookup"><span data-stu-id="a61ca-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a61ca-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a61ca-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a61ca-121">Copiar componentes</span><span class="sxs-lookup"><span data-stu-id="a61ca-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="a61ca-122">Crear una nueva aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="a61ca-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="a61ca-123">Eliminar una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="a61ca-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="a61ca-124">Instalación de nuevos componentes</span><span class="sxs-lookup"><span data-stu-id="a61ca-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="a61ca-125">Mover componentes</span><span class="sxs-lookup"><span data-stu-id="a61ca-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="a61ca-126">Quitar un componente de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="a61ca-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



