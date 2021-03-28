---
description: Los elementos del panel de control son archivos dll o archivos ejecutables (. exe) que permiten a los usuarios configurar el entorno de Windows. Normalmente se accede a ellos haciendo clic en un icono del panel de control.
title: Implementar elementos del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984343"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="ab9fd-104">Implementar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="ab9fd-105">Los elementos del panel de control son archivos dll o archivos ejecutables (. exe) que permiten a los usuarios configurar el entorno de Windows.</span><span class="sxs-lookup"><span data-stu-id="ab9fd-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="ab9fd-106">Normalmente se accede a ellos haciendo clic en un icono del panel de control.</span><span class="sxs-lookup"><span data-stu-id="ab9fd-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="ab9fd-107">En esta sección se describen los elementos del panel de control y se explica cómo crearlos y registrarlos para que aparezcan correctamente en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="ab9fd-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="ab9fd-108">En Windows Vista, se incluye información que indica cómo agregar vínculos de tareas que aparecen bajo el elemento del panel de control y en los resultados de la búsqueda del panel de control.</span><span class="sxs-lookup"><span data-stu-id="ab9fd-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="ab9fd-109">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="ab9fd-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="ab9fd-110">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="ab9fd-111">Cómo registrar elementos del panel de control ejecutable</span><span class="sxs-lookup"><span data-stu-id="ab9fd-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="ab9fd-112">Cómo registrar elementos del panel de control DLL</span><span class="sxs-lookup"><span data-stu-id="ab9fd-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="ab9fd-113">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="ab9fd-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="ab9fd-114">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="ab9fd-115">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="ab9fd-116">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="ab9fd-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="ab9fd-117">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="ab9fd-118">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="ab9fd-119">Acceder al panel de control en modo seguro</span><span class="sxs-lookup"><span data-stu-id="ab9fd-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="ab9fd-120">Nombres canónicos de los elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="ab9fd-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



