---
description: Windows El instalador implementa una serie de controles estándar que los autores de paquetes pueden colocar en los cuadros de diálogo. Sin embargo, no todos los controles estándar Windows microsoft están disponibles y no se pueden crear controles personalizados para su uso con la interfaz de usuario del instalador.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Información general sobre los controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee9d03f0f21f9cc0611a1fae4831b6ccbbda9f40eda873cdf4c26b259ec43f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638527"
---
# <a name="controls-overview"></a>Información general sobre los controles

Windows El instalador implementa una serie de controles estándar que los autores de paquetes pueden colocar en los cuadros de diálogo. Sin embargo, no todos los controles estándar Windows microsoft están disponibles y no se pueden crear controles personalizados para su uso con la interfaz de usuario del instalador.

Los controles se crean en los cuadros de diálogo del instalador de una manera similar a cómo se crean los cuadros de diálogo mediante programación mediante la API de interfaz de usuario de Microsoft Windows. Se crea un control a partir de una plantilla registrada en la tabla Control. Esta plantilla es ligeramente diferente en que contiene el nombre único del cuadro de diálogo en el que aparece el control.

En la API Windows interfaz de usuario de Microsoft, la interacción del usuario se realiza mediante la creación de una función de devolución de llamada para controlar los mensajes publicados por el control . Además, la mayoría de los Windows de Microsoft reciben mensajes, como los enviados por la [función SendMessage.](/windows/win32/api/winuser/nf-winuser-sendmessage)

La comunicación entre el usuario y los controles se realiza en el instalador mediante el uso de [ControlEvents](controlevent-overview.md). Sin embargo, hay un conjunto limitado de ControlEvents que son específicos de cada control en el conjunto limitado de controles de Windows Installer. Los controles pueden publicar más de un control ControlEvent y pueden recibir más de un control ControlEvent.

Los controles pueden publicar eventos ControlEvent específicos mediante el uso de la tabla ControlEvent. Los controles pueden recibir ControlEvents mediante el uso de la [tabla EventMapping](eventmapping-table.md).

Windows El instalador también publica ControlEvents durante la ejecución de algunas acciones y los controles suscritos a estos ControlEvents en la tabla EventMapping los reciben.

 

 
