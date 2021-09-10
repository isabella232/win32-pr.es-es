---
title: Mensajes y funciones de controlador instalables
description: Mensajes y funciones de controlador instalables
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- controladores instalables, funciones
- controladores instalables, mensajes
- controladores instalables, función OpenDriver
- Función OpenDriver
- controladores instalables, mensajes personalizados
- mensajes de controlador
- mensajes de controladores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372296"
---
# <a name="installable-driver-functions-and-messages"></a>Mensajes y funciones de controlador instalables

Puede abrir un controlador instalable desde una aplicación mediante la [**función OpenDriver.**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) Esta función crea una instancia del controlador, cargando el controlador en la memoria si no existe ninguna otra instancia, y devuelve el identificador de la nueva instancia. Al abrir un controlador instalable, debe proporcionar la ruta de acceso completa del controlador o los nombres de la clave del Registro y el valor asociados al controlador.

Una vez abierto un controlador, puede dirigirlo para que realice tareas mediante la [**función SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) para enviar mensajes de controlador al controlador. Por ejemplo, puede dirigir al controlador para que muestre su cuadro de diálogo de configuración mediante el envío del [**mensaje DRV \_ CONFIGURE.**](drv-configure.md) Antes de enviar este mensaje, debe determinar si el controlador tiene un cuadro de diálogo de configuración mediante el envío del mensaje [**\_ QUERYCONFIGURE**](drv-queryconfigure.md) de DRV y la comprobación de un valor devuelto distinto de cero. Muchos controladores proporcionan un conjunto de mensajes personalizados que puede enviar para dirigir las operaciones del controlador.

Si necesita acceso especial a un controlador instalable, como el acceso a sus recursos, puede recuperar el identificador del módulo del controlador mediante la [**función GetDriverModuleHandle.**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)

Cuando ya no necesite el controlador instalable, puede cerrarlo mediante la [**función CloseDriver.**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver)

Puede usar las funciones de controlador instalables y los mensajes para abrir y administrar cualquier controlador instalable. Sin embargo, el curso de acción recomendado para abrir y administrar dispositivos multimedia es usar primero servicios estándar (como [**waveOutOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)y [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para dispositivos de salida de forma de onda), si existen. Si no existen servicios estándar para un controlador multimedia, abra y administre el controlador mediante las funciones de controlador instalables y los mensajes.

> [!Note]  
> Las [**funciones SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) y [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) son las funciones preferidas que se usan para enviar mensajes a un controlador y para obtener un identificador a una instancia de módulo. Sin embargo, la función [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) anterior se ha incluido para mantener la compatibilidad con versiones anteriores del Windows operativo.

 

 

 