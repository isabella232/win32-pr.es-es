---
description: En esta sección se describe la creación de menús contextuales (contexto) y la implementación de controladores de menú contextual (verbo).
title: Menús contextuales y controladores de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275243"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="824ab-103">Menús contextuales y controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="824ab-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="824ab-104">En esta sección se describe la creación de menús contextuales (contexto) y la implementación de controladores de menú contextual (verbo).</span><span class="sxs-lookup"><span data-stu-id="824ab-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="824ab-105">Esta sección sobre los tipos de archivo y las asociaciones de archivo está organizada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="824ab-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="824ab-106">Verbos y asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="824ab-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="824ab-107">Elegir un método de menú contextual estático o dinámico</span><span class="sxs-lookup"><span data-stu-id="824ab-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="824ab-108">Prácticas recomendadas para los controladores de menú contextual y varios verbos</span><span class="sxs-lookup"><span data-stu-id="824ab-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="824ab-109">Crear controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="824ab-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="824ab-110">Crear menús en cascada estáticos</span><span class="sxs-lookup"><span data-stu-id="824ab-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="824ab-111">Cómo suprimir y controlar la visibilidad de los verbos</span><span class="sxs-lookup"><span data-stu-id="824ab-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="824ab-112">Cómo emplear el modelo de selección de verbos</span><span class="sxs-lookup"><span data-stu-id="824ab-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="824ab-113">Cómo usar atributos de elemento</span><span class="sxs-lookup"><span data-stu-id="824ab-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="824ab-114">Cómo implementar verbos personalizados para carpetas a través de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="824ab-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="824ab-115">Personalización de un menú contextual mediante verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="824ab-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="824ab-116">Cómo implementar la interfaz IContextMenu</span><span class="sxs-lookup"><span data-stu-id="824ab-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="824ab-117">Referencia del menú contextual</span><span class="sxs-lookup"><span data-stu-id="824ab-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="824ab-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="824ab-118">Additional Resources</span></span>

<span data-ttu-id="824ab-119">Para obtener información sobre los conceptos relacionados, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="824ab-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="824ab-120">[Introducción a las asociaciones de archivo](fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="824ab-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="824ab-121">Para extender el shell con controladores de tipo de archivo, vea [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="824ab-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="824ab-122">Para crear un almacén de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="824ab-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="824ab-123">Para obtener documentación de referencia relacionada, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="824ab-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="824ab-124">Para ejecutar un verbo en un elemento de Shell, vea el método [**InvokeVerb**](folderitem-invokeverb.md) .</span><span class="sxs-lookup"><span data-stu-id="824ab-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="824ab-125">Para recuperar una colección de verbos que se pueden ejecutar en un elemento de Shell, vea el método [**verbs**](folderitem-verbs.md) .</span><span class="sxs-lookup"><span data-stu-id="824ab-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="824ab-126">Para realizar una operación en un archivo especificado, vea las funciones [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="824ab-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



