---
title: Elegir cuándo crear objetos accesibles
description: Los desarrolladores de servidores pueden crear todos los objetos accesibles dentro de un contenedor cuando se crea el contenedor o pueden crear objetos accesibles dinámicamente.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076014"
---
# <a name="choosing-when-to-create-accessible-objects"></a><span data-ttu-id="1e4b3-103">Elegir cuándo crear objetos accesibles</span><span class="sxs-lookup"><span data-stu-id="1e4b3-103">Choosing When to Create Accessible Objects</span></span>

<span data-ttu-id="1e4b3-104">Los desarrolladores de servidores pueden crear todos los objetos accesibles dentro de un contenedor cuando se crea el contenedor o pueden crear objetos accesibles dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-104">Server developers can create all the accessible objects within a container when the container is created, or they can create the accessible objects dynamically.</span></span>

<span data-ttu-id="1e4b3-105">Por ejemplo, Imagine un cuadro de diálogo con varios controles personalizados.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-105">For example, imagine a dialog box with several custom controls.</span></span> <span data-ttu-id="1e4b3-106">Un servidor crea objetos accesibles para todos los controles personalizados cuando se muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-106">A server creates accessible objects for all of the custom controls when the dialog box is displayed.</span></span> <span data-ttu-id="1e4b3-107">Sin embargo, si uno de los controles es un cuadro combinado personalizado, el servidor espera hasta que un usuario lo seleccione para crear objetos accesibles para los elementos que contiene el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-107">However, if one of the controls is a custom combo box, the server waits until a user selects it to create accessible objects for the items that the combo box contains.</span></span>

<span data-ttu-id="1e4b3-108">Al hacer que el elemento primario cree objetos accesibles dinámicamente, las aplicaciones usan menos memoria que si todos los objetos accesibles posibles se crearon con anterioridad.</span><span class="sxs-lookup"><span data-stu-id="1e4b3-108">By having the parent create accessible objects dynamically, applications use less memory than if all the possible accessible objects were created ahead of time.</span></span>

 

 




