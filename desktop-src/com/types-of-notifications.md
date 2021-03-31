---
title: Tipos de notificaciones
description: Tipos de notificaciones
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418975"
---
# <a name="types-of-notifications"></a><span data-ttu-id="e0a7a-103">Tipos de notificaciones</span><span class="sxs-lookup"><span data-stu-id="e0a7a-103">Types of Notifications</span></span>

<span data-ttu-id="e0a7a-104">Las notificaciones se dividen en tres grupos: documento compuesto, datos y vista.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="e0a7a-105">Un objeto envía notificaciones de documentos compuestos en respuesta a que se les cambia el nombre, se guardan, se cierran o, en el caso de un vínculo, se cambia el nombre del origen del vínculo.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="e0a7a-106">Como cabría esperar, los objetos envían notificaciones de datos en respuesta a los cambios en sus datos y envían notificaciones de vista en respuesta a los cambios en su presentación.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="e0a7a-107">Las aplicaciones de contenedor se deben registrar por separado para cada uno de estos tipos de notificación, pero todo se puede controlar mediante un único receptor de consulta.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="e0a7a-108">Todos los contenedores, el controlador de objetos y el objeto vinculado se registran para las notificaciones de documentos compuestos.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="e0a7a-109">El contenedor típico también se registra para las notificaciones de vista.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="e0a7a-110">Las notificaciones de datos normalmente se envían al objeto vinculado y al controlador de objetos.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="e0a7a-111">Un contenedor de propósito especial, como uno que representa los datos en sí, puede beneficiarse de la recepción de notificaciones de datos en lugar de ver las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="e0a7a-112">Por ejemplo, un contenedor de gráficos incrustado con un vínculo a una tabla puede registrarse para recibir notificaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="e0a7a-113">Dado que un cambio en la tabla afecta al gráfico, la recepción de una notificación de datos dirigiría el contenedor para obtener los nuevos datos tabulares.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0a7a-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0a7a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0a7a-115">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="e0a7a-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 




