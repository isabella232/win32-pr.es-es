---
title: Mensajes de controlador
description: Mensajes de controlador
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- controladores instalables, mensajes
- controladores instalables, mensajes personalizados
- mensajes de controlador
- mensajes de controladores personalizados
- controladores instalables, función DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372211"
---
# <a name="driver-messages"></a>Mensajes de controlador

Cada mensaje de controlador consta de un identificador de mensaje y dos parámetros de 32 bits. El identificador del mensaje es un valor único que la [función DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) comprueba para determinar qué acción realizar. El significado de los parámetros del mensaje depende del mensaje. Los parámetros pueden representar valores o direcciones. En muchos casos, los parámetros no se usan y se establecen en cero.

Los mensajes de controlador pueden ser estándar o personalizados. Windows envía mensajes de controlador estándar, como [**DRV \_ OPEN,**](drv-open.md) [**DRV \_ CLOSE**](drv-close.md)y [**DRV \_ CONFIGURE**](drv-configure.md), a un controlador instalable en respuesta a una solicitud para abrir, cerrar o configurar el controlador. Los mensajes estándar dirigen al controlador instalable a cargar o descargar sus recursos, habilitar o deshabilitar su operación, abrir o cerrar una instancia de controlador y mostrar un cuadro de diálogo de configuración. Algunos mensajes estándar, como [**DRV \_ POWER**](drv-power.md) y [**DRV \_ EXITSESSION,**](drv-exitsession.md)notifican al controlador los eventos de todo el sistema que afectan al funcionamiento del controlador o a cualquier hardware relacionado.

Las aplicaciones y los archivos DLL envían mensajes de controlador personalizados para dirigir un controlador instalable para llevar a cabo acciones específicas del controlador. Los controladores instalables que admiten mensajes personalizados deben incluir el procesamiento adecuado en la **función DriverProc.** Para evitar conflictos entre mensajes de controlador estándar y personalizados, los identificadores de mensajes personalizados deben tener valores que van desde DRV \_ RESERVED hasta DRV \_ USER. Los mensajes personalizados pasados a la función [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) se omiten.

 

 