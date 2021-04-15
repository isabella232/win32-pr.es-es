---
description: Windows Installer implementa un número de controles estándar que los autores de paquetes pueden colocar en los cuadros de diálogo. Sin embargo, no todos los controles estándar de Microsoft Windows están disponibles y no se pueden crear controles personalizados para usarlos con la interfaz de usuario del instalador.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Información general sobre los controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669751"
---
# <a name="controls-overview"></a>Información general sobre los controles

Windows Installer implementa un número de controles estándar que los autores de paquetes pueden colocar en los cuadros de diálogo. Sin embargo, no todos los controles estándar de Microsoft Windows están disponibles y no se pueden crear controles personalizados para usarlos con la interfaz de usuario del instalador.

Los controles se crean en los cuadros de diálogo del instalador de manera similar a cómo se crean los cuadros de diálogo mediante programación con la API de la interfaz de usuario de Microsoft Windows. Se crea un control a partir de una plantilla registrada en la tabla de control. Esta plantilla es ligeramente diferente en que contiene el nombre único del cuadro de diálogo en el que aparece el control.

En la API de la interfaz de usuario de Microsoft Windows, la interacción con el usuario se logra mediante la creación de una función de devolución de llamada para controlar los mensajes enviados por el control. Además, la mayoría de los controles de Microsoft Windows reciben mensajes, como los enviados por la función [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .

La comunicación entre el usuario y los controles se realiza en el instalador mediante el uso de [ControlEvents](controlevent-overview.md). Sin embargo, hay un conjunto limitado de ControlEvents que son específicos de cada control en el conjunto limitado de controles de Windows Installer. Los controles pueden publicar más de un ControlEvent, y pueden recibir más de un ControlEvent,.

Los controles pueden publicar ControlEvents específicos mediante el uso de la tabla ControlEvent,. Los controles pueden recibir ControlEvents mediante el uso de la [tabla EventMapping](eventmapping-table.md).

Windows Installer publica ControlEvents durante la ejecución de algunas acciones también y los controles suscritos a estos ControlEvents en la tabla EventMapping los reciben.

 

 
