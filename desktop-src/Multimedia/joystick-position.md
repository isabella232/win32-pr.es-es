---
title: Posición del joystick
description: Posición del joystick
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- joysticks, posición
- joysticks, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271136"
---
# <a name="joystick-position"></a>Posición del joystick

Puede consultar un joystick para obtener información sobre la posición y el botón mediante la función [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Por ejemplo, una aplicación puede consultar el joystick para obtener valores de posición de línea de base. La hoja de propiedades del panel de control joystick utiliza esta técnica al calibrar el joystick.

También puede consultar un joystick u otro dispositivo que tenga capacidades extendidas mediante la función [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 