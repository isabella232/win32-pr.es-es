---
description: Las clases RealTimeStylus, GestureRecognizer y DynamicRenderer se implementan como contenedores COM y solo están disponibles en código administrado.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Notas de implementación para las API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000979"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="eb3e3-103">Notas de implementación para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="eb3e3-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="eb3e3-104">Las clases [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))y [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) se implementan como contenedores com y solo están disponibles en código administrado.</span><span class="sxs-lookup"><span data-stu-id="eb3e3-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="eb3e3-105">Cuando el objeto [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))o [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) se agrega como un complemento a un objeto **RealTimeStylus** , los objetos com subyacentes interactúan en el nivel com.</span><span class="sxs-lookup"><span data-stu-id="eb3e3-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="eb3e3-106">Por lo tanto, no se admite la llamada directa a los métodos de las interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) o [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="eb3e3-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="eb3e3-107">Agregar el objeto **RealTimeStylus**, GestureRecognizer o DynamicRenderer al objeto **RealTimeStylus** es la única manera de tener acceso a estas características.</span><span class="sxs-lookup"><span data-stu-id="eb3e3-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
