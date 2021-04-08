---
description: Para agregar componentes a la carpeta componentes de una aplicación COM+, puede utilizar el Asistente para instalación de componentes COM+ o arrastrar archivos. dll que contengan los componentes del explorador de Windows y colocarlos en la aplicación.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Instalación de nuevos componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080232"
---
# <a name="installing-new-components"></a><span data-ttu-id="7c882-103">Instalación de nuevos componentes</span><span class="sxs-lookup"><span data-stu-id="7c882-103">Installing New Components</span></span>

<span data-ttu-id="7c882-104">Para agregar componentes a la carpeta **componentes** de una aplicación com+, puede utilizar el Asistente para instalación de componentes com+ o arrastrar archivos. dll que contengan los componentes del explorador de Windows y colocarlos en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c882-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="7c882-105">Si usa el Asistente para instalación de componentes COM+, puede instalar un nuevo componente, que registra el componente en el equipo, o importar los componentes que ya se han registrado.</span><span class="sxs-lookup"><span data-stu-id="7c882-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="7c882-106">Los componentes se pueden agregar a aplicaciones vacías o a aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="7c882-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="7c882-107">**Para agregar un componente a una aplicación COM+**</span><span class="sxs-lookup"><span data-stu-id="7c882-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="7c882-108">En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo que hospeda la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="7c882-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="7c882-109">Abra la carpeta **aplicaciones com+** para ese equipo y seleccione la aplicación en la que desea instalar los componentes.</span><span class="sxs-lookup"><span data-stu-id="7c882-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="7c882-110">Abra la carpeta de la aplicación y seleccione **componentes**.</span><span class="sxs-lookup"><span data-stu-id="7c882-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="7c882-111">En el menú **acción** , seleccione **nuevo** y, a continuación, haga clic en **componente**.</span><span class="sxs-lookup"><span data-stu-id="7c882-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="7c882-112">También puede hacer clic con el botón secundario en la carpeta **componentes** , seleccionar **nuevo** y, a continuación, hacer clic en **componente**.</span><span class="sxs-lookup"><span data-stu-id="7c882-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="7c882-113">En la página **principal** del Asistente para instalación de aplicaciones com+, haga clic en **siguiente** y, en el cuadro de diálogo **importar o instalar un componente** , haga clic en **instalar nuevos componentes** .</span><span class="sxs-lookup"><span data-stu-id="7c882-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="7c882-114">En el cuadro de diálogo **instalar nuevos componentes** , haga clic en **Agregar** para buscar el componente que desee agregar.</span><span class="sxs-lookup"><span data-stu-id="7c882-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="7c882-115">En el cuadro de diálogo **seleccionar archivos para instalar** , escriba el nombre de archivo del componente que se va a instalar o seleccione un nombre de archivo de la lista que se muestra.</span><span class="sxs-lookup"><span data-stu-id="7c882-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="7c882-116">Haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="7c882-116">Click **Open**.</span></span>

    <span data-ttu-id="7c882-117">Después de agregar los archivos, el cuadro de diálogo **instalar nuevos componentes** muestra los archivos que ha agregado y sus componentes asociados.</span><span class="sxs-lookup"><span data-stu-id="7c882-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="7c882-118">Si activa la casilla **detalles** , verá más información sobre el contenido de los archivos y los componentes que se encontraron.</span><span class="sxs-lookup"><span data-stu-id="7c882-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="7c882-119">Los componentes COM sin configurar deben tener una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="7c882-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="7c882-120">Si COM+ no encuentra la biblioteca de tipos del componente, el componente no aparecerá en la lista.</span><span class="sxs-lookup"><span data-stu-id="7c882-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="7c882-121">También puede quitar un archivo de la lista **archivos para instalar** seleccionándolo y haciendo clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="7c882-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="7c882-122">Haga clic en **siguiente** y, a continuación, haga clic en **Finalizar** para instalar el componente.</span><span class="sxs-lookup"><span data-stu-id="7c882-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c882-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c882-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c882-124">Copiar componentes</span><span class="sxs-lookup"><span data-stu-id="7c882-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="7c882-125">Crear una nueva aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="7c882-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="7c882-126">Eliminar una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="7c882-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="7c882-127">Importar componentes</span><span class="sxs-lookup"><span data-stu-id="7c882-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="7c882-128">Mover componentes</span><span class="sxs-lookup"><span data-stu-id="7c882-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="7c882-129">Quitar un componente de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="7c882-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



