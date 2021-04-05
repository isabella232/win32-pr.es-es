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
# <a name="configuration-windows-multimedia"></a>Configuración (Windows multimedia)

Un controlador instalable puede permitir que los usuarios elijan la configuración para el controlador y el hardware asociado mediante la presentación de un cuadro de diálogo de configuración al procesar el mensaje de configuración de [**DRV \_**](drv-configure.md) . El controlador es responsable de la creación y administración del cuadro de diálogo, el procesamiento de los datos proporcionados por el usuario en el cuadro de diálogo y el cambio de la configuración del controlador o el hardware solicitado por el usuario. El controlador debe proporcionar un procedimiento de cuadro de diálogo independiente para procesar los mensajes de ventana para el cuadro de diálogo y una plantilla de cuadro de diálogo para definir la apariencia y el contenido del cuadro de diálogo.

Antes de recibir el \_ mensaje de configuración de DRV, un controlador recibe el mensaje [**DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md) . El controlador debe devolver un valor distinto de cero a la consulta para garantizar la recepción del mensaje de configuración de DRV subsiguiente \_ .

Al inicializar el cuadro de diálogo Configuración, el controlador normalmente recupera información de configuración del registro. Para ayudar a encontrar esta información, el \_ mensaje de configuración de DRV incluye normalmente la dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contiene los nombres de la clave del registro y el valor asociado al controlador. Si el usuario solicita cambios a la configuración, el controlador debe actualizar la información de configuración en el registro.

 

 
