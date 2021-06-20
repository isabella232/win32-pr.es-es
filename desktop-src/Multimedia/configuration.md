---
title: Configuración (Windows Multimedia)
description: Obtenga información sobre cómo un controlador multimedia de Windows puede permitir que los usuarios elijan opciones de configuración mediante la visualización de un cuadro de diálogo de configuración.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- controladores instalables, configuración
- controladores instalables, DRV_CONFIGURE mensaje
- DRV_CONFIGURE mensaje
- DRV_QUERYCONFIGURE mensaje
- Mensaje DRVCONFIGINFO
- configuración de controladores instalables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403928"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="bbecb-109">Configuración (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="bbecb-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="bbecb-110">Un controlador instalable puede permitir que los usuarios elijan opciones de configuración para el controlador y el hardware asociado mediante la visualización de un cuadro de diálogo de configuración al procesar el [**mensaje DE CONFIGURACIÓN \_ de DRV.**](drv-configure.md)</span><span class="sxs-lookup"><span data-stu-id="bbecb-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="bbecb-111">El controlador es responsable de crear y administrar el cuadro de diálogo, procesar cualquier entrada de usuario desde el cuadro de diálogo y cambiar la configuración del controlador o hardware según lo solicitado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bbecb-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="bbecb-112">El controlador debe proporcionar un procedimiento de cuadro de diálogo independiente para procesar mensajes de ventana para el cuadro de diálogo y una plantilla de cuadro de diálogo para definir la apariencia y el contenido del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bbecb-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="bbecb-113">Antes de recibir el mensaje \_ DRV CONFIGURE, un controlador recibe el [**mensaje \_ QUERYCONFIGURE de DRV.**](drv-queryconfigure.md)</span><span class="sxs-lookup"><span data-stu-id="bbecb-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="bbecb-114">El controlador debe devolver un valor distinto de cero a la consulta para garantizar la recepción del mensaje DRV \_ CONFIGURE posterior.</span><span class="sxs-lookup"><span data-stu-id="bbecb-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="bbecb-115">Al inicializar el cuadro de diálogo de configuración, el controlador normalmente recupera información de configuración del Registro.</span><span class="sxs-lookup"><span data-stu-id="bbecb-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="bbecb-116">Para ayudar a localizar esta información, el mensaje DRV CONFIGURE normalmente incluye la dirección de una estructura \_ [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del Registro y el valor asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="bbecb-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="bbecb-117">Si el usuario solicita cambios en la configuración, el controlador debe actualizar la información de configuración en el Registro.</span><span class="sxs-lookup"><span data-stu-id="bbecb-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
