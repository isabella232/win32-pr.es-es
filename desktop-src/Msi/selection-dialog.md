---
description: Este cuadro de diálogo modal permite a los usuarios seleccionar elementos determinados.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Cuadro de diálogo de selección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653082"
---
# <a name="selection-dialog"></a><span data-ttu-id="f8bb1-103">Cuadro de diálogo de selección</span><span class="sxs-lookup"><span data-stu-id="f8bb1-103">Selection Dialog</span></span>

<span data-ttu-id="f8bb1-104">Este cuadro de diálogo modal permite a los usuarios seleccionar elementos determinados.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="f8bb1-105">Un cuadro de diálogo de selección contiene un [control SelectionTree](selectiontree-control.md) que publica varios ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="f8bb1-106">Normalmente, estos ControlEvents se suscriben a mediante controles de [texto](text-control.md), [icono](icon-control.md)o [mapa de bits](bitmap-control.md) que muestran una descripción, el tamaño, la ruta de acceso y el icono del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="f8bb1-107">Hay un [control Pushbutton](pushbutton-control.md) en el cuadro de diálogo que publica [SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md) y genera un [cuadro de diálogo de exploración](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="f8bb1-108">El control de exploración permite al usuario seleccionar un directorio.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="f8bb1-109">El árbol de selección se rellena solo después de que se llame a la acción [CostInitialize](costinitialize-action.md) y a la [acción CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bb1-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="f8bb1-110">Un cuadro de diálogo de selección se usa normalmente para seleccionar características.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="f8bb1-111">Las características se enumeran como elementos en un control SelectionTree y se etiquetan con la cadena corta de texto que aparece en la columna title de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="f8bb1-112">La cadena de texto de la columna Descripción de la tabla de características se publica como [SelectionDescription ControlEvent,](selectiondescription-controlevent.md) y se muestra en un [control de texto](text-control.md) en el cuadro de diálogo de selección.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="f8bb1-113">El control de árbol de selección también publica el identificador en el icono del elemento resaltado.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 



