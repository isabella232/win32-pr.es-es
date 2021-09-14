---
title: La marca Notify
description: La marca Notify
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260687"
---
# <a name="the-notify-flag"></a>La marca Notify

La marca "notify" (MCI NOTIFY) indica al dispositivo que publique un mensaje \_ [**MM MCIDETIFY**](mm-mcinotify.md) cuando el dispositivo complete una acción. La aplicación debe tener un procedimiento de ventana para procesar el mensaje \_ MM MTIFTIFY para que la notificación tenga algún efecto. Un mensaje MM MTIFTIFY indica que se ha completado el procesamiento de un comando, pero no indica si el comando se completó correctamente, no se pudo completar o se \_ anuló.

La aplicación especifica el identificador de la ventana de destino del mensaje cuando emite un comando. En la interfaz de cadena de comandos, este identificador es el último parámetro de la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85)) En la interfaz command-message, el identificador se especifica en la palabra de orden bajo del **miembro dwCallBack** de la estructura enviada con el mensaje de comando. (Cada estructura asociada a un mensaje de comando contiene este miembro).

 

 