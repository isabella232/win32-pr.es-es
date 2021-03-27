---
description: Cuando se proporciona una vista previa, deben seguirse las siguientes directrices.
title: Instrucciones de controlador de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910770"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="af2ff-103">Instrucciones de controlador de vista previa</span><span class="sxs-lookup"><span data-stu-id="af2ff-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="af2ff-104">Cuando se proporciona una vista previa, deben seguirse las siguientes directrices.</span><span class="sxs-lookup"><span data-stu-id="af2ff-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="af2ff-105">Una vista previa debe contener una interfaz de usuario mínima; es simplemente una vista previa.</span><span class="sxs-lookup"><span data-stu-id="af2ff-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="af2ff-106">Debería mostrar solo el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="af2ff-106">It should display only the file content.</span></span> <span data-ttu-id="af2ff-107">No debe mostrar cuadros de diálogo, pantallas de presentación, barras de herramientas o paneles de tareas.</span><span class="sxs-lookup"><span data-stu-id="af2ff-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="af2ff-108">El panel de lectura se usará normalmente junto con la búsqueda para identificar rápidamente un archivo.</span><span class="sxs-lookup"><span data-stu-id="af2ff-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="af2ff-109">Cualquier cosa que esté abarrotando el panel de lectura o que, de otro modo, se destrae del contenido del archivo o provoca retrasos en la presentación de la vista previa debe evitarse.</span><span class="sxs-lookup"><span data-stu-id="af2ff-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="af2ff-110">La vista previa debe permitir al usuario navegar por el documento.</span><span class="sxs-lookup"><span data-stu-id="af2ff-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="af2ff-111">El usuario también debe poder seleccionar y copiar texto.</span><span class="sxs-lookup"><span data-stu-id="af2ff-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="af2ff-112">La vista previa no debe consumir mucha memoria, debe consumir recursos mínimos y debe tener un tiempo de inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="af2ff-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="af2ff-113">Se debe bloquear la ejecución de todos los scripts y macros del archivo en el que se va a obtener una vista previa para la seguridad y la privacidad.</span><span class="sxs-lookup"><span data-stu-id="af2ff-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="af2ff-114">La vista previa debe admitir aceleradores de teclado para la navegación y la selección que admite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="af2ff-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="af2ff-115">También debe mostrar un menú contextual al hacer clic con el botón secundario.</span><span class="sxs-lookup"><span data-stu-id="af2ff-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="af2ff-116">Cuando un archivo se muestra como una vista previa, la vista previa no debe bloquear el archivo.</span><span class="sxs-lookup"><span data-stu-id="af2ff-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="af2ff-117">Se puede obtener una vista previa de un archivo y abrirlo en la aplicación asociada al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="af2ff-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af2ff-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af2ff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2ff-119">Controladores de vista previa y host de vista previa de Shell</span><span class="sxs-lookup"><span data-stu-id="af2ff-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="af2ff-120">Crear controladores de vista previa</span><span class="sxs-lookup"><span data-stu-id="af2ff-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



