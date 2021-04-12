---
title: Marca de notificación
description: Marca de notificación
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420673"
---
# <a name="the-notify-flag"></a>Marca de notificación

La marca "notificar" (notificación de MCI \_ ) indica al dispositivo que envíe un mensaje [**mm MCINOTIFY**](mm-mcinotify.md) cuando el dispositivo completa una acción. La aplicación debe tener un procedimiento de ventana para procesar el \_ mensaje de MCINOTIFY mm para que la notificación surta efecto. Un \_ mensaje de MCINOTIFY mm indica que el procesamiento de un comando se ha completado, pero no indica si el comando se completó correctamente, produjo un error o se sustituyó o anuló.

La aplicación especifica el identificador de la ventana de destino para el mensaje cuando emite un comando. En la interfaz de cadena de comandos, este identificador es el último parámetro de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . En la interfaz de mensaje de comando, el identificador se especifica en la palabra de orden inferior del miembro **dwCallBack** de la estructura enviada con el mensaje de comando. (Cada estructura asociada con un mensaje de comando contiene este miembro).

 

 