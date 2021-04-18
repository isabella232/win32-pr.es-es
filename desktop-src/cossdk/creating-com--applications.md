---
description: Crear aplicaciones COM+
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: Crear aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705391"
---
# <a name="creating-com-applications"></a><span data-ttu-id="e914d-103">Crear aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-103">Creating COM+ Applications</span></span>

<span data-ttu-id="e914d-104">En esta sección se describe cómo crear una nueva aplicación COM+ (vacía) y, a continuación, agregar componentes a dicha aplicación.</span><span class="sxs-lookup"><span data-stu-id="e914d-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="e914d-105">También se describe cómo agregar componentes COM a y quitarlos de las aplicaciones COM+ existentes, y cómo mover y copiar componentes de una aplicación COM+ a otra.</span><span class="sxs-lookup"><span data-stu-id="e914d-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="e914d-106">Tema</span><span class="sxs-lookup"><span data-stu-id="e914d-106">Topic</span></span>                                                                                                       | <span data-ttu-id="e914d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e914d-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e914d-108">Crear una nueva aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="e914d-109">Describe cómo crear una nueva aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="e914d-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="e914d-110">Instalación de nuevos componentes</span><span class="sxs-lookup"><span data-stu-id="e914d-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="e914d-111">Describe cómo instalar nuevos componentes de.</span><span class="sxs-lookup"><span data-stu-id="e914d-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="e914d-112">Importar componentes</span><span class="sxs-lookup"><span data-stu-id="e914d-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="e914d-113">Describe cómo importar componentes de.</span><span class="sxs-lookup"><span data-stu-id="e914d-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="e914d-114">Quitar un componente de una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="e914d-115">Describe cómo eliminar un componente de una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="e914d-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="e914d-116">Mover componentes</span><span class="sxs-lookup"><span data-stu-id="e914d-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="e914d-117">Describe cómo trasladar un componente de una aplicación COM+ a otra.</span><span class="sxs-lookup"><span data-stu-id="e914d-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="e914d-118">Copiar componentes</span><span class="sxs-lookup"><span data-stu-id="e914d-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="e914d-119">Describe cómo copiar un componente de una aplicación COM+ a otra.</span><span class="sxs-lookup"><span data-stu-id="e914d-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="e914d-120">Eliminar una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="e914d-121">Describe cómo eliminar una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="e914d-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="e914d-122">Para obtener información conceptual acerca de los procedimientos descritos en esta sección, consulte [información general de la aplicación com+](com--application-overview.md) e [implementación de aplicaciones com+](deploying-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="e914d-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="e914d-123">Para obtener información de procedimientos sobre las tareas administrativas relacionadas con la exportación e instalación de aplicaciones COM+, vea el tema sobre la instalación de aplicaciones COM+ en la guía del administrador de servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="e914d-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e914d-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e914d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e914d-125">Automatizar la administración de COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="e914d-126">Configurar aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e914d-127">Conversión de paquetes MTS en aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="e914d-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




