---
title: Sesiones de edición
description: Cuando un servicio de texto debe obtener, modificar o establecer texto en un contexto, debe solicitar una sesión de edición.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Marco de trabajo de servicios de texto (TSF), editar sesión
- TSF (marco de trabajo de servicios de texto), editar sesión
- servicios de texto, editar sesión
- sesión de edición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532434"
---
# <a name="edit-sessions"></a><span data-ttu-id="a825e-107">Sesiones de edición</span><span class="sxs-lookup"><span data-stu-id="a825e-107">Edit Sessions</span></span>

<span data-ttu-id="a825e-108">Cuando un servicio de texto debe obtener, modificar o establecer texto en un contexto, debe solicitar una *sesión de edición*.</span><span class="sxs-lookup"><span data-stu-id="a825e-108">When a text service must obtain, modify, or set text in a context, it must request an *edit session*.</span></span> <span data-ttu-id="a825e-109">Cuando se solicita una sesión de edición, el administrador de TSF negocia con el propietario del contexto de destino un bloqueo de documento del tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="a825e-109">When an edit session is requested, the TSF manager negotiates with the owner of the target context for a document lock of the requested type.</span></span> <span data-ttu-id="a825e-110">Cuando se concede el bloqueo del documento, el administrador de TSF permite al servicio de texto leer o escribir texto en el contexto o desde él.</span><span class="sxs-lookup"><span data-stu-id="a825e-110">When the document lock is granted, the TSF manager enables the text service to read and/or write text to or from the context.</span></span>

 

 




