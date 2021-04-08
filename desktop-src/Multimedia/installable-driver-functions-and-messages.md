---
title: Mensajes y funciones de controlador instalables
description: Mensajes y funciones de controlador instalables
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- Controladores instalables, funciones
- Controladores instalables, mensajes
- Controladores instalables, función OpenDriver
- OpenDriver función)
- Controladores instalables, mensajes personalizados
- mensajes de controlador
- mensajes de controlador personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995215"
---
# <a name="installable-driver-functions-and-messages"></a>Mensajes y funciones de controlador instalables

Puede abrir un controlador instalable desde una aplicación mediante la función [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) . Esta función crea una instancia del controlador, carga el controlador en memoria si no existe ninguna otra instancia y devuelve el identificador de la nueva instancia. Al abrir un controlador instalable, debe proporcionar la ruta de acceso completa del controlador o los nombres de la clave del registro y el valor asociado al controlador.

Una vez abierto un controlador, puede dirigirlo para llevar a cabo tareas mediante la función [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) para enviar mensajes de controlador al controlador. Por ejemplo, puede dirigir el controlador para que muestre su cuadro de diálogo de configuración mediante el envío del mensaje [**DRV \_ Configure**](drv-configure.md) . Antes de enviar este mensaje, debe determinar si el controlador tiene un cuadro de diálogo de configuración mediante el envío del mensaje [**DRV \_ QUERYCONFIGURE**](drv-queryconfigure.md) y la comprobación de un valor devuelto distinto de cero. Muchos controladores proporcionan un conjunto de mensajes personalizados que puede enviar para dirigir las operaciones del controlador.

Si necesita acceso especial a un controlador instalable, como el acceso a sus recursos, puede recuperar el identificador de módulo del controlador mediante la función [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) .

Cuando ya no necesite el controlador instalable, puede cerrarlo mediante la función [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) .

Puede utilizar las funciones y los mensajes del controlador instalable para abrir y administrar cualquier controlador instalable. Sin embargo, el curso de acción recomendado para abrir y administrar dispositivos multimedia es usar primero servicios estándar (como [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)y [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para dispositivos de salida de forma de onda), si existen. Si los servicios estándar no existen para un controlador multimedia, abra y administre el controlador mediante las funciones y los mensajes del controlador instalable.

> [!Note]  
> Las funciones [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) y [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) son las funciones preferidas que se usan para enviar mensajes a un controlador y para obtener un identificador para una instancia de módulo. La función [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) anterior, sin embargo, se ha incluido para mantener la compatibilidad con las versiones anteriores del sistema operativo Windows.

 

 

 