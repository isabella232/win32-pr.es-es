---
description: La acción CreateShortcuts administra la creación de accesos directos.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Acción CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083232"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="ad67b-103">Acción CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="ad67b-103">CreateShortcuts Action</span></span>

<span data-ttu-id="ad67b-104">La acción CreateShortcuts administra la creación de accesos directos.</span><span class="sxs-lookup"><span data-stu-id="ad67b-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ad67b-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="ad67b-105">Sequence Restrictions</span></span>

<span data-ttu-id="ad67b-106">La acción CreateShortcuts debe aparecer después de la acción [InstallFiles](installfiles-action.md) y la acción [RemoveShortcuts](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ad67b-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ad67b-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="ad67b-107">ActionData Messages</span></span>



| <span data-ttu-id="ad67b-108">Campo</span><span class="sxs-lookup"><span data-stu-id="ad67b-108">Field</span></span> | <span data-ttu-id="ad67b-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="ad67b-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="ad67b-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ad67b-110">\[1\]</span></span> | <span data-ttu-id="ad67b-111">Identificador del acceso directo creado.</span><span class="sxs-lookup"><span data-stu-id="ad67b-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ad67b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad67b-112">Remarks</span></span>

<span data-ttu-id="ad67b-113">La acción CreateShortcuts crea accesos directos a los archivos de clave de los componentes de las características que se seleccionan para la instalación o el anuncio.</span><span class="sxs-lookup"><span data-stu-id="ad67b-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad67b-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad67b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad67b-115">Tabla de acceso directo</span><span class="sxs-lookup"><span data-stu-id="ad67b-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="ad67b-116">Tabla MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="ad67b-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



