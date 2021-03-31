---
title: Mensajes de controlador
description: Mensajes de controlador
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- Controladores instalables, mensajes
- Controladores instalables, mensajes personalizados
- mensajes de controlador
- mensajes de controlador personalizados
- Controladores instalables, función DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077616"
---
# <a name="driver-messages"></a><span data-ttu-id="93efd-108">Mensajes de controlador</span><span class="sxs-lookup"><span data-stu-id="93efd-108">Driver Messages</span></span>

<span data-ttu-id="93efd-109">Cada mensaje de controlador consta de un identificador de mensaje y de parámetros de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="93efd-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="93efd-110">El identificador de mensaje es un valor único que la función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) comprueba para determinar la acción que se va a llevar a cabo. El significado de los parámetros del mensaje depende del mensaje.</span><span class="sxs-lookup"><span data-stu-id="93efd-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="93efd-111">Los parámetros pueden representar valores o direcciones.</span><span class="sxs-lookup"><span data-stu-id="93efd-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="93efd-112">En muchos casos, no se usan los parámetros y se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="93efd-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="93efd-113">Los mensajes del controlador pueden ser estándar o personalizados.</span><span class="sxs-lookup"><span data-stu-id="93efd-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="93efd-114">Windows envía mensajes de controlador estándar, como [**DRV \_ Open**](drv-open.md), [**DRV \_ Close**](drv-close.md)y [**DRV \_ Configure**](drv-configure.md), a un controlador instalable en respuesta a una solicitud para abrir, cerrar o configurar el controlador.</span><span class="sxs-lookup"><span data-stu-id="93efd-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="93efd-115">Los mensajes estándar dirigen al controlador instalable para cargar o descargar sus recursos, habilitar o deshabilitar su funcionamiento, abrir o cerrar una instancia de controlador y mostrar un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="93efd-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="93efd-116">Algunos mensajes estándar, como [**DRV \_ Power**](drv-power.md) y [**DRV \_ EXITSESSION**](drv-exitsession.md), notifican al controlador los eventos de todo el sistema que afectan al funcionamiento del controlador o a cualquier hardware relacionado.</span><span class="sxs-lookup"><span data-stu-id="93efd-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="93efd-117">Las aplicaciones y los archivos dll envían mensajes de controlador personalizados para dirigir un controlador instalable para llevar a cabo acciones específicas del controlador.</span><span class="sxs-lookup"><span data-stu-id="93efd-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="93efd-118">Los controladores instalables que admiten mensajes personalizados deben incluir el procesamiento adecuado en la función **DriverProc** .</span><span class="sxs-lookup"><span data-stu-id="93efd-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="93efd-119">Para evitar conflictos entre los mensajes de controladores personalizados y estándar, los identificadores de mensajes personalizados deben tener valores comprendidos entre DRV \_ reservado y el \_ usuario DRV.</span><span class="sxs-lookup"><span data-stu-id="93efd-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="93efd-120">Se omiten los mensajes personalizados pasados a la función [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="93efd-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 