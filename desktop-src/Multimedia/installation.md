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
# <a name="installation-windows-multimedia"></a>Instalación (Windows multimedia)

Un controlador instalable puede llevar a cabo tareas de instalación específicas del controlador al procesar los mensajes de [**\_ instalación de DRV**](drv-install.md) y [**DRV \_ Remove**](drv-remove.md) . Una aplicación de instalación, como una aplicación del panel de control, envía los mensajes al controlador al instalar o quitar el controlador, respectivamente.

Al procesar el mensaje de instalación de DRV \_ , el controlador comprueba normalmente que el hardware necesario está presente y, a continuación, muestra el cuadro de diálogo de configuración para permitir que el usuario elija la configuración inicial para el controlador y el hardware asociado. El mensaje incluye la dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del registro y el valor asociado al controlador. el controlador comprueba el valor del registro para obtener información de configuración predeterminada. Por último, el controlador también crea las claves del registro y los valores adicionales necesarios para una operación correcta.

Al procesar el \_ mensaje DRV Remove, el controlador quita las claves y los valores del registro que se hayan creado.

 

 
