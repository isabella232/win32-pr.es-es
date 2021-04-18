---
description: En los temas de esta sección se proporcionan las especificaciones de referencia para las funciones de pila de entrada de dispositivo de puntero.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funciones (pila de entrada de dispositivo de puntero)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721649"
---
# <a name="pointer-device-input-stack-functions"></a>Funciones de pila de entrada de dispositivo de puntero

En los temas de esta sección se proporcionan las especificaciones de referencia para las funciones de [pila de entrada de dispositivo de puntero](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Configura el dispositivo de inserción de punteros para la aplicación que realiza la llamada e inicializa el número máximo de punteros simultáneos que puede insertar la aplicación.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Destruye el dispositivo de inyección de puntero especificado.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Obtiene información sobre el dispositivo de puntero.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Obtiene los identificadores de cursor que se asignan a los cursores asociados a un dispositivo de puntero.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Obtiene las propiedades del dispositivo que no se incluyen en la estructura de [**\_ \_ información del dispositivo de puntero**](/previous-versions/windows/desktop/api) . <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Obtiene el intervalo x e y para el dispositivo de puntero (en himetric) y el intervalo x e y (resolución actual) de la pantalla a la que está asignado el dispositivo de puntero. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Obtiene información acerca de los dispositivos de puntero conectados al sistema.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Obtiene los datos de entrada sin formato del dispositivo de puntero. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simula la entrada de puntero (lápiz o toque).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registra una ventana para procesar las notificaciones de dispositivo de [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)y [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) puntero.<br/> |

## <a name="related-topics"></a>Temas relacionados

[Referencia de la pila de entrada de dispositivo de puntero](unified-input-stack-reference.md)
