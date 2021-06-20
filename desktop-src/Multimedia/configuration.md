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
# <a name="configuration-windows-multimedia"></a>Configuración (Windows Multimedia)

Un controlador instalable puede permitir que los usuarios elijan opciones de configuración para el controlador y el hardware asociado mediante la visualización de un cuadro de diálogo de configuración al procesar el [**mensaje DE CONFIGURACIÓN \_ de DRV.**](drv-configure.md) El controlador es responsable de crear y administrar el cuadro de diálogo, procesar cualquier entrada de usuario desde el cuadro de diálogo y cambiar la configuración del controlador o hardware según lo solicitado por el usuario. El controlador debe proporcionar un procedimiento de cuadro de diálogo independiente para procesar mensajes de ventana para el cuadro de diálogo y una plantilla de cuadro de diálogo para definir la apariencia y el contenido del cuadro de diálogo.

Antes de recibir el mensaje \_ DRV CONFIGURE, un controlador recibe el [**mensaje \_ QUERYCONFIGURE de DRV.**](drv-queryconfigure.md) El controlador debe devolver un valor distinto de cero a la consulta para garantizar la recepción del mensaje DRV \_ CONFIGURE posterior.

Al inicializar el cuadro de diálogo de configuración, el controlador normalmente recupera información de configuración del Registro. Para ayudar a localizar esta información, el mensaje DRV CONFIGURE normalmente incluye la dirección de una estructura \_ [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del Registro y el valor asociados al controlador. Si el usuario solicita cambios en la configuración, el controlador debe actualizar la información de configuración en el Registro.

 

 
