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
# <a name="driver-messages"></a>Mensajes de controlador

Cada mensaje de controlador consta de un identificador de mensaje y de parámetros de 2 32 bits. El identificador de mensaje es un valor único que la función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) comprueba para determinar la acción que se va a llevar a cabo. El significado de los parámetros del mensaje depende del mensaje. Los parámetros pueden representar valores o direcciones. En muchos casos, no se usan los parámetros y se establecen en cero.

Los mensajes del controlador pueden ser estándar o personalizados. Windows envía mensajes de controlador estándar, como [**DRV \_ Open**](drv-open.md), [**DRV \_ Close**](drv-close.md)y [**DRV \_ Configure**](drv-configure.md), a un controlador instalable en respuesta a una solicitud para abrir, cerrar o configurar el controlador. Los mensajes estándar dirigen al controlador instalable para cargar o descargar sus recursos, habilitar o deshabilitar su funcionamiento, abrir o cerrar una instancia de controlador y mostrar un cuadro de diálogo de configuración. Algunos mensajes estándar, como [**DRV \_ Power**](drv-power.md) y [**DRV \_ EXITSESSION**](drv-exitsession.md), notifican al controlador los eventos de todo el sistema que afectan al funcionamiento del controlador o a cualquier hardware relacionado.

Las aplicaciones y los archivos dll envían mensajes de controlador personalizados para dirigir un controlador instalable para llevar a cabo acciones específicas del controlador. Los controladores instalables que admiten mensajes personalizados deben incluir el procesamiento adecuado en la función **DriverProc** . Para evitar conflictos entre los mensajes de controladores personalizados y estándar, los identificadores de mensajes personalizados deben tener valores comprendidos entre DRV \_ reservado y el \_ usuario DRV. Se omiten los mensajes personalizados pasados a la función [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .

 

 