---
title: Instalación (Windows multimedia)
description: Instalación
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- Controladores instalables, instalar
- Controladores instalables, DRV_INSTALL mensaje
- Controladores instalables, DRV_REMOVE mensaje
- Mensaje DRV_INSTALL
- Mensaje DRV_REMOVE
- Mensaje DRVCONFIGINFO
- instalación de controladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421800"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="32aff-110">Instalación (Windows multimedia)</span><span class="sxs-lookup"><span data-stu-id="32aff-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="32aff-111">Un controlador instalable puede llevar a cabo tareas de instalación específicas del controlador al procesar los mensajes de [**\_ instalación de DRV**](drv-install.md) y [**DRV \_ Remove**](drv-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="32aff-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="32aff-112">Una aplicación de instalación, como una aplicación del panel de control, envía los mensajes al controlador al instalar o quitar el controlador, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="32aff-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="32aff-113">Al procesar el mensaje de instalación de DRV \_ , el controlador comprueba normalmente que el hardware necesario está presente y, a continuación, muestra el cuadro de diálogo de configuración para permitir que el usuario elija la configuración inicial para el controlador y el hardware asociado.</span><span class="sxs-lookup"><span data-stu-id="32aff-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="32aff-114">El mensaje incluye la dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del registro y el valor asociado al controlador. el controlador comprueba el valor del registro para obtener información de configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="32aff-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="32aff-115">Por último, el controlador también crea las claves del registro y los valores adicionales necesarios para una operación correcta.</span><span class="sxs-lookup"><span data-stu-id="32aff-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="32aff-116">Al procesar el \_ mensaje DRV Remove, el controlador quita las claves y los valores del registro que se hayan creado.</span><span class="sxs-lookup"><span data-stu-id="32aff-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
