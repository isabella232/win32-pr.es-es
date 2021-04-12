---
title: Parámetro de duración del mensaje
description: Las aplicaciones suelen usar ventanas emergentes para mostrar brevemente mensajes de notificación importantes para el usuario. Una aplicación crea la ventana, la muestra para una duración definida por la aplicación y, a continuación, destruye la ventana.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420840"
---
# <a name="message-duration-parameter"></a>Parámetro de duración del mensaje

Las aplicaciones suelen usar ventanas emergentes para mostrar brevemente mensajes de notificación importantes para el usuario. Una aplicación crea la ventana, la muestra para una duración definida por la aplicación y, a continuación, destruye la ventana.

Dado que los usuarios con discapacidades visuales o condiciones cognitivas pueden necesitar más tiempo para leer los elementos emergentes de notificación, las aplicaciones no deben codificar la duración. En su lugar, una aplicación debe establecer la duración según el valor del parámetro del sistema **SPI \_ GETMESSAGEDURATION** . Para recuperar este parámetro, use la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

Las aplicaciones de tecnología de asistencia pueden establecer la duración del mensaje, en función de los datos proporcionados por el usuario, estableciendo el parámetro del sistema **SPI \_ SETMESSAGEDURATION** .

 

 