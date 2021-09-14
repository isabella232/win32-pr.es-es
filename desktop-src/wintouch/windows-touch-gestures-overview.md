---
title: Windows Información general sobre gestos táctiles
description: En esta sección se describen los distintos gestos admitidos por Windows Touch.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows Táctil, gestos
- gestos, acerca de
- Windows Touch, compatibilidad heredada
- gestos, compatibilidad heredada
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 2290477aa8b26e937fe6d5f300ed1fea32872f5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247431"
---
# <a name="windows-touch-gestures-overview"></a>Windows Información general sobre gestos táctiles

En esta sección se describen los distintos gestos admitidos por Windows Touch.

## <a name="gestures-overview"></a>Información general sobre gestos

Windows La función táctil permite varios gestos que admiten uno y varios contactos. En la imagen siguiente se muestran los distintos gestos que se admiten en Windows 7.

![ilustración que muestra los gestos que windows touch admite en Windows 7](images/gestures.png)

> [!Note]  
> Algunos reconocedores son más confiables en la interpretación de gestos con varios contactos cuando los contactos están más separados entre sí.

## <a name="legacy-support"></a>Compatibilidad heredada

Para la compatibilidad heredada, el controlador de gestos predeterminado asigna algunos gestos a Windows mensajes que se usaron en versiones anteriores de Windows. En la tabla siguiente se describe cómo se asignan los gestos a los mensajes heredados.

| Gesto        | Descripción  | Mensajes generados              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Movimiento panorámico            | El gesto de desplazamiento horizontal se asigna al uso de la rueda de desplazamiento.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Mantener presionado | El gesto de mantener presionado se asigna a hacer clic con el botón derecho en el mouse.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | El gesto de zoom desencadena mensajes similares a mantener presionada la tecla CTRL y girar la rueda del mouse para desplazarse. | **WM_MOUSEWHEEL** con **MK_CONTROL** en *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretación Windows gestos táctiles

Windows Los desarrolladores de aplicaciones pueden interpretar los gestos táctiles controlando [**WM_GESTURE**](wm-gesture.md) mensaje de la función WndProc de una aplicación. Después de controlar este mensaje, puede recuperar una [**estructura GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) que describe el gesto. La **estructura GESTUREINFO** tendrá información variada que depende del tipo de gesto.

La [**estructura GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) se recupera pasando el identificador a la estructura de información de gestos a la [**función GetGestureInfo.**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)

Las marcas siguientes indican los distintos estados de los gestos y se almacenan en *dwFlags*. 

| Nombre        | Value      | Descripción                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Se está iniciando un gesto.           |
| GF_INERTIA | 0x00000002 | Un gesto ha desencadenado la inercia. |
| GF_END     | 0x00000004 | Ha finalizado un gesto.          |

> [!Note]  
> La mayoría de las aplicaciones **deben omitir GID_BEGIN** y **GID_END** y pasarlas [a DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). El controlador de gestos predeterminado usa estos mensajes. El comportamiento de la aplicación es indefinido **cuando GID_BEGIN** y **GID_END** los mensajes son consumidos por una aplicación de terceros.

En la tabla siguiente se indican los distintos identificadores de los gestos. 

| Nombre              | Value | Descripción                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Se está iniciando un gesto.      |
| GID_END          | 2     | Un gesto está finalizando.        |
| GID_ZOOM         | 3     | Gesto de zoom.           |
| GID_PAN          | 4     | Gesto de panorámica.            |
| GID_ROTATE       | 5     | Gesto de rotación.       |
| GID_TWOFINGERTAP | 6     | Gesto de pulsar con dos dedos. |
| GID_PRESSANDTAP  | 7     | Gesto de pulsar y presionar.  |

> [!Note]  
> El **GID_PAN** gesto tiene inercia integrada. Al final de un gesto de panorámica, el sistema operativo crea mensajes de gesto de panorámica adicionales.

Los miembros de la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** y **ullArguments** especifican un punto (mediante la estructura **POINTS)** e información adicional sobre los gestos en función del gesto. En la tabla siguiente se enumeran los valores asociados a cada tipo de gesto.

| Identificador de gesto            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indica la distancia entre los dos puntos.            | Indica el centro del zoom.   |
| **GID_PAN**          | Indica la distancia entre los dos puntos.            | Indica la posición actual del panorámica.                    |
| **GID_ROTATE**       | Indica el ángulo de rotación si se **establece GF_BEGIN** marca de rotación. De lo contrario, este es el cambio de ángulo desde que se inició la rotación. Se firma para indicar la dirección de la rotación. Use las [**macros GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) [**y GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obtener y establecer el valor de ángulo. | Esto indica el centro de la rotación, que es el punto estacional en el que se gira el objeto de destino. |
| **GID_TWOFINGERTAP** | Indica la distancia entre los dos dedos.           | Indica el centro de los dos dedos.                      |
| **GID_PRESSANDTAP**  | Indica la diferencia entre el primer dedo y el segundo dedo. Este valor se almacena en una **estructura POINT** en los 32 bits inferiores del *miembro ullArguments.*                        | Indica la posición en la que baja el primer dedo.   |

## <a name="related-topics"></a>Temas relacionados

[Windows Gestos táctiles](guide-multi-touch-gestures.md)