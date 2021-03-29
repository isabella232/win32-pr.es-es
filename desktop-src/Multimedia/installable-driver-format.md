---
title: Formato del controlador instalable
description: Formato del controlador instalable
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- Controladores instalables, formatos
- Controladores instalables, función DriverProc
- Controladores instalables, mensajes
- mensajes de controlador
- formatos de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358914"
---
# <a name="installable-driver-format"></a><span data-ttu-id="b2cda-108">Formato del controlador instalable</span><span class="sxs-lookup"><span data-stu-id="b2cda-108">Installable Driver Format</span></span>

<span data-ttu-id="b2cda-109">Cada controlador instalable exporta una función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) .</span><span class="sxs-lookup"><span data-stu-id="b2cda-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="b2cda-110">Esta función de punto de entrada común recibe *mensajes de controlador* del sistema que dirigen al controlador para llevar a cabo acciones o proporcionar información.</span><span class="sxs-lookup"><span data-stu-id="b2cda-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="b2cda-111">El sistema envía mensajes de controlador a la función **DriverProc** cuando una aplicación o dll abre o cierra el controlador o solicita que se envíe un mensaje al controlador.</span><span class="sxs-lookup"><span data-stu-id="b2cda-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="b2cda-112">La función **DriverProc** procesa el mensaje o pasa el mensaje al controlador de mensajes predeterminado, la función [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="b2cda-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="b2cda-113">En cualquier caso, **DriverProc** debe devolver un valor que indique si la acción solicitada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2cda-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 