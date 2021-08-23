---
description: Los temas de esta sección proporcionan las especificaciones de referencia para las funciones pila de entrada de dispositivo de puntero.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funciones (pila de entrada del dispositivo de puntero)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 5101847d78f396edcb317986ab3d95d578dabdfe12197531787115f49c9a69a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611745"
---
# <a name="pointer-device-input-stack-functions"></a>Funciones de pila de entrada de dispositivo de puntero

Los temas de esta sección proporcionan las especificaciones de referencia para las [funciones pila de entrada de dispositivo de](pointer-device-stack-portal.md) puntero.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Configura el dispositivo de inyección de puntero para la aplicación que realiza la llamada e inicializa el número máximo de punteros simultáneos que la aplicación puede insertar.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Destruye el dispositivo de inyección de puntero especificado.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Obtiene información sobre el dispositivo de puntero.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Obtiene los iDs de cursor asignados a los cursores asociados a un dispositivo de puntero.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Obtiene las propiedades de dispositivo que no se incluyen en la estructura [**POINTER \_ DEVICE \_ INFO.**](/previous-versions/windows/desktop/api) <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Obtiene el intervalo x e y para el dispositivo de puntero (en himetric) y el intervalo x e y (resolución actual) para la pantalla a la que está asignado el dispositivo de puntero. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Obtiene información sobre los dispositivos de puntero asociados al sistema.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Obtiene los datos de entrada sin procesar del dispositivo de puntero. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simula la entrada de puntero (lápiz o entrada táctil).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registra una ventana para procesar las notificaciones [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)y [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) dispositivo de puntero.<br/> |

## <a name="related-topics"></a>Temas relacionados

[Referencia de pila de entrada de dispositivo de puntero](unified-input-stack-reference.md)
