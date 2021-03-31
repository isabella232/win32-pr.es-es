---
title: Información general sobre los gestos táctiles de Windows
description: En esta sección se describen los distintos gestos admitidos por Touch de Windows.
ms.assetid: b2fa11a7-9abb-4149-96e3-e8c663c29d4a
keywords:
- Windows Touch, gestos
- gestos, acerca de
- Windows Touch, compatibilidad heredada
- gestos, compatibilidad heredada
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 2290477aa8b26e937fe6d5f300ed1fea32872f5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078042"
---
# <a name="windows-touch-gestures-overview"></a>Información general sobre los gestos táctiles de Windows

En esta sección se describen los distintos gestos admitidos por Touch de Windows.

## <a name="gestures-overview"></a>Información general sobre gestos

La función táctil de Windows permite varios gestos que admiten contactos únicos y múltiples. En la imagen siguiente se muestran los distintos gestos que se admiten en Windows 7.

![Ilustración que muestra los gestos que Windows Touch admite en Windows 7](images/gestures.png)

> [!Note]  
> Algunos reconocedores son más confiables en la interpretación de gestos con varios contactos cuando los contactos están más alejados entre sí.

## <a name="legacy-support"></a>Compatibilidad heredada

Para la compatibilidad heredada, el controlador de gestos predeterminado asigna algunos gestos a los mensajes de Windows que se usaron en versiones anteriores de Windows. En la tabla siguiente se describe cómo se asignan los gestos a los mensajes heredados.

| Gesto        | Descripción  | Mensajes generados              |
|----------------|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Movimiento panorámico            | El gesto de panorámica se asigna a mediante la rueda de desplazamiento.                  | **WM_VSCROLL**<br/> **WM_HSCROLL**<br/>       |
| Mantener presionado | El gesto de mantener presionado se asigna para hacer clic con el botón secundario del mouse.     | **WM_RBUTTONDOWN**<br/> **WM_RBUTTONUP**<br/> |
| Zoom           | El gesto de zoom desencadena mensajes similares a los que contienen la tecla CTRL y gira la rueda del mouse para desplazarse. | **WM_MOUSEWHEEL** con **MK_CONTROL** establecido en *lParam* |

## <a name="interpreting-windows-touch-gestures"></a>Interpretar los gestos táctiles de Windows

Los desarrolladores de aplicaciones pueden interpretar los gestos táctiles de Windows mediante el control del mensaje de [**WM_GESTURE**](wm-gesture.md) desde la función WndProc de una aplicación. Después de controlar este mensaje, puede recuperar una estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) que describe el gesto. La estructura **GESTUREINFO** tendrá una información ordenada que depende del tipo de gesto.

La estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) se recupera pasando el identificador a la estructura de información de gestos a la función [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) .

Las marcas siguientes indican los distintos Estados de los gestos y se almacenan en *dwFlags*. 

| Nombre        | Value      | Descripción                      |
|-------------|------------|----------------------------------|
| GF_BEGIN   | 0x00000001 | Se está iniciando un gesto.           |
| GF_INERTIA | 0x00000002 | Un gesto ha desencadenado la inercia. |
| GF_END     | 0x00000004 | Ha finalizado un gesto.          |

> [!Note]  
> La mayoría de las aplicaciones deben omitir el **GID_BEGIN** y **GID_END** y pasarlos a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Estos mensajes los utiliza el controlador de gestos predeterminado. El comportamiento de la aplicación no está definido cuando una aplicación de terceros consume los mensajes **GID_BEGIN** y **GID_END** .

En la tabla siguiente se indican los distintos identificadores de gestos. 

| Nombre              | Value | Descripción                 |
|-------------------|-------|-----------------------------|
| GID_BEGIN        | 1     | Se está iniciando un gesto.      |
| GID_END          | 2     | Un gesto está finalizando.        |
| GID_ZOOM         | 3     | Gesto de zoom.           |
| GID_PAN          | 4     | Movimiento de la panorámica.            |
| GID_ROTATE       | 5     | El movimiento de rotación.       |
| GID_TWOFINGERTAP | 6     | El gesto de puntear dos dedos. |
| GID_PRESSANDTAP  | 7     | Gesto de presionar y pulsar.  |

> [!Note]  
> El gesto de **GID_PAN** tiene inercia integrada. Al final de un gesto de panorámica, el sistema operativo crea mensajes de movimiento de pan adicionales.

Los miembros de la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) **ptsLocation** y **ullArguments** especifican un punto (mediante la estructura **Points** ) e información adicional sobre los gestos según el gesto. En la tabla siguiente se enumeran los valores asociados a cada tipo de gesto.

| IDENTIFICADOR de gesto            | *ullArguments*                  | *ptsLocation*                       |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID_ZOOM**         | Indica la distancia entre los dos puntos.            | Indica el centro del zoom.   |
| **GID_PAN**          | Indica la distancia entre los dos puntos.            | Indica la posición actual de la panorámica.                    |
| **GID_ROTATE**       | Indica el ángulo de rotación si se establece la marca de **GF_BEGIN** . De lo contrario, este es el cambio de ángulo desde que se ha iniciado la rotación. Está firmado para indicar la dirección de la rotación. Use las macros [**GID_ROTATE_ANGLE_FROM_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) y [**GID_ROTATE_ANGLE_TO_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obtener y establecer el valor del ángulo. | Indica el centro del giro, que es el punto estacionario en el que se gira el objeto de destino. |
| **GID_TWOFINGERTAP** | Indica la distancia entre los dos dedos.           | Indica el centro de los dos dedos.                      |
| **GID_PRESSANDTAP**  | Indica la diferencia entre el primer dedo y el segundo dedo. Este valor se almacena en una estructura de **punto** en los 32 bits inferiores del miembro *ullArguments* .                        | Indica la posición en la que se activa el primer dedo.   |

## <a name="related-topics"></a>Temas relacionados

[Gestos táctiles de Windows](guide-multi-touch-gestures.md)