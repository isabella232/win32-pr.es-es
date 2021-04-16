---
title: Compatibilidad con In-Process
description: La implementación actual de la anotación dinámica está completamente en proceso y, por consiguiente, solo permite que el proceso que posee esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356840"
---
# <a name="in-process-support"></a><span data-ttu-id="99d3b-103">Compatibilidad con In-Process</span><span class="sxs-lookup"><span data-stu-id="99d3b-103">In-Process Support</span></span>

<span data-ttu-id="99d3b-104">La implementación actual de la anotación dinámica está completamente en proceso y, por consiguiente, solo permite que el proceso que posee esos elementos de la interfaz de usuario anote los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="99d3b-104">The current implementation of Dynamic Annotation is entirely in-process and consequently allows only UI elements to be annotated by the process that owns those UI elements.</span></span> <span data-ttu-id="99d3b-105">No es posible que un proceso anote los elementos de la interfaz de usuario de otro proceso.</span><span class="sxs-lookup"><span data-stu-id="99d3b-105">It is not possible for one process to annotate the UI elements of another process.</span></span>

<span data-ttu-id="99d3b-106">Tenga en cuenta que esto solo afecta a la acción de establecer una anotación; no interfiere con la posibilidad de que los clientes tengan acceso a las propiedades (anotadas o de otro tipo) de los elementos de la interfaz de usuario en otros procesos.</span><span class="sxs-lookup"><span data-stu-id="99d3b-106">Note that this only affects the act of setting an annotation; it does not interfere with the ability of clients to access the properties (annotated or otherwise) of UI elements in other processes.</span></span>

 

 




