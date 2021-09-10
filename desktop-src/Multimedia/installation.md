---
title: Instalación (Windows Multimedia)
description: Obtenga información sobre Windows multimedia, incluido el procesamiento de DRV_INSTALL y DRV_REMOVE mensajes.
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372301"
---
# <a name="installation-windows-multimedia"></a>Instalación (Windows Multimedia)

Un controlador instalable puede llevar a cabo tareas de instalación específicas del controlador al procesar los mensajes [**DRV \_ INSTALL**](drv-install.md) y [**DRV \_ REMOVE.**](drv-remove.md) Una aplicación de instalación, como una Panel de control, envía los mensajes al controlador al instalar o quitar el controlador, respectivamente.

Al procesar el mensaje DRV INSTALL, el controlador normalmente comprueba que el hardware necesario está presente y, a continuación, muestra el cuadro de diálogo de configuración para permitir que el usuario elija los valores de configuración iniciales para el controlador y el \_ hardware asociado. El mensaje incluye la dirección de una [**estructura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del Registro y el valor asociados al controlador. el controlador comprueba el valor del Registro para obtener información de configuración predeterminada. Por último, el controlador también crea las claves y los valores del Registro adicionales necesarios para el funcionamiento correcto.

Al procesar el mensaje REMOVE de DRV, el controlador quita las claves del \_ Registro y los valores que puede haber creado.

 

 
