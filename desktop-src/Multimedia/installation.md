---
title: Instalación (Windows Multimedia)
description: Obtenga información sobre la instalación multimedia de Windows, incluido el procesamiento de DRV_INSTALL y DRV_REMOVE mensajes.
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- controladores instalables, instalación
- controladores instalables, DRV_INSTALL mensaje
- controladores instalables, DRV_REMOVE mensaje
- DRV_INSTALL mensaje
- DRV_REMOVE mensaje
- Mensaje DRVCONFIGINFO
- instalar controladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f82a23a781e62553d6488331b2c832104fd770
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989040"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="b82db-110">Instalación (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="b82db-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="b82db-111">Un controlador instalable puede llevar a cabo tareas de instalación específicas del controlador al procesar los mensajes [**DRV \_ INSTALL**](drv-install.md) [**y DRV \_ REMOVE.**](drv-remove.md)</span><span class="sxs-lookup"><span data-stu-id="b82db-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="b82db-112">Una aplicación de instalación, como una Panel de control, envía los mensajes al controlador al instalar o quitar el controlador, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b82db-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="b82db-113">Al procesar el mensaje DRV INSTALL, el controlador normalmente comprueba que el hardware necesario está presente y, a continuación, muestra el cuadro de diálogo de configuración para permitir que el usuario elija los valores de configuración iniciales para el controlador y el \_ hardware asociado.</span><span class="sxs-lookup"><span data-stu-id="b82db-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="b82db-114">El mensaje incluye la dirección de una [**estructura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del Registro y el valor asociados al controlador; el controlador comprueba el valor del Registro para obtener información de configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b82db-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="b82db-115">Por último, el controlador también crea las claves y los valores del Registro adicionales necesarios para una operación correcta.</span><span class="sxs-lookup"><span data-stu-id="b82db-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="b82db-116">Al procesar el mensaje REMOVE de DRV, el controlador quita las claves y los valores del Registro \_ que haya creado.</span><span class="sxs-lookup"><span data-stu-id="b82db-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
