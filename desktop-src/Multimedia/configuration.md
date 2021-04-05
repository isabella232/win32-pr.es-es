---
title: Configuración (Windows multimedia)
description: Configuración
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- Controladores instalables, configuración
- Controladores instalables, DRV_CONFIGURE mensaje
- Mensaje DRV_CONFIGURE
- Mensaje DRV_QUERYCONFIGURE
- Mensaje DRVCONFIGINFO
- configuración de controladores instalables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078726"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="cc7f1-109">Configuración (Windows multimedia)</span><span class="sxs-lookup"><span data-stu-id="cc7f1-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="cc7f1-110">Un controlador instalable puede permitir que los usuarios elijan la configuración para el controlador y el hardware asociado mediante la presentación de un cuadro de diálogo de configuración al procesar el mensaje de configuración de [**DRV \_**](drv-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="cc7f1-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="cc7f1-111">El controlador es responsable de la creación y administración del cuadro de diálogo, el procesamiento de los datos proporcionados por el usuario en el cuadro de diálogo y el cambio de la configuración del controlador o el hardware solicitado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cc7f1-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="cc7f1-112">El controlador debe proporcionar un procedimiento de cuadro de diálogo independiente para procesar los mensajes de ventana para el cuadro de diálogo y una plantilla de cuadro de diálogo para definir la apariencia y el contenido del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc7f1-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="cc7f1-113">Antes de recibir el \_ mensaje de configuración de DRV, un controlador recibe el mensaje [**DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="cc7f1-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="cc7f1-114">El controlador debe devolver un valor distinto de cero a la consulta para garantizar la recepción del mensaje de configuración de DRV subsiguiente \_ .</span><span class="sxs-lookup"><span data-stu-id="cc7f1-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="cc7f1-115">Al inicializar el cuadro de diálogo Configuración, el controlador normalmente recupera información de configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="cc7f1-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="cc7f1-116">Para ayudar a encontrar esta información, el \_ mensaje de configuración de DRV incluye normalmente la dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del registro y el valor asociado al controlador.</span><span class="sxs-lookup"><span data-stu-id="cc7f1-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="cc7f1-117">Si el usuario solicita cambios a la configuración, el controlador debe actualizar la información de configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="cc7f1-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
