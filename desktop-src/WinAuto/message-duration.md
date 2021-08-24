---
title: Parámetro de duración del mensaje
description: Las aplicaciones suelen usar ventanas emergentes para mostrar brevemente mensajes de notificación importantes al usuario. Una aplicación crea la ventana, la muestra durante una duración definida por la aplicación y, a continuación, destruye la ventana.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2657f71c60a489fbedffdf2730dd37f388b749f27fa68ac57e039b2f27d5f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828293"
---
# <a name="message-duration-parameter"></a>Parámetro de duración del mensaje

Las aplicaciones suelen usar ventanas emergentes para mostrar brevemente mensajes de notificación importantes al usuario. Una aplicación crea la ventana, la muestra durante una duración definida por la aplicación y, a continuación, destruye la ventana.

Dado que los usuarios con discapacidades visuales o condiciones cognitivas pueden necesitar más tiempo para leer los elementos emergentes de notificación, las aplicaciones no deben codificar de forma permanente la duración. En su lugar, una aplicación debe establecer la duración en función del valor del parámetro del sistema **SPI \_ GETMESSAGEDURATION.** Para recuperar este parámetro, use la [**función SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

Las aplicaciones de tecnología de asistencia pueden establecer la duración del mensaje, en función de la entrada del usuario, estableciendo el parámetro del sistema **SPI \_ SETMESSAGEDURATION.**

 

 