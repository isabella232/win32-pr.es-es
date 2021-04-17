---
title: Identificador DPI_AWARENESS_CONTEXT (WINDEF. h)
description: Identifica el contexto de reconocimiento para una ventana.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359748"
---
# <a name="dpi_awareness_context-handle"></a>Identificador de contexto de \_ reconocimiento de PPP \_

Identifica el contexto de reconocimiento para una ventana.

## <a name="syntax"></a>Sintaxis

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Constantes

**contexto de reconocimiento de PPP no \_ \_ \_ compatible**<dl> PPP no compatible. Esta ventana no escala para los cambios de PPP y siempre se supone que tiene un factor de escala del 100% (96 PPP). El sistema lo escalará automáticamente con cualquier otro valor de PPP.  
</dl>

**conocimiento \_ \_ del sistema de contexto de reconocimiento de \_ PPP \_**<dl> Reconocimiento de PPP del sistema. Esta ventana no escala para los cambios de PPP. Consultará el valor de PPP una vez y lo utilizará durante la vigencia del proceso. Si cambia el valor de PPP, el proceso no se ajustará al nuevo valor de PPP. El sistema se escala o reduce verticalmente de forma automática cuando cambia el valor de PPP del valor del sistema.  
</dl>

**contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor \_**<dl> Con reconocimiento de PPP por monitor. Esta ventana comprueba el PPP cuando se crea y ajusta el factor de escala cada vez que cambia el PPP. El sistema no escala automáticamente estos procesos.  
</dl>

**Contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor \_ compatible con \_ V2**<dl> También se conoce como **por monitor V2**. Un avance sobre el modo de reconocimiento de PPP por monitor original, que permite a las aplicaciones tener acceso a nuevos comportamientos de escalado relacionados con los PPP en cada ventana de nivel superior.  
Por monitor V2 estaba disponible en la actualización de Creators de Windows 10 y no está disponible en versiones anteriores del sistema operativo.  
Los comportamientos adicionales introducidos son los siguientes:

-   **Notificaciones de cambio de PPP de ventana secundaria** : en los contextos de cada monitor V2, se notifica a todo el árbol de la ventana todos los cambios de PPP que se produzcan.
-   **Escalado de área no cliente** : todas las ventanas tendrán automáticamente el área no cliente dibujada con distinción de PPP. No es necesario realizar llamadas a [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) .
-   **Escalado de menús de Win32** : todos los menús de Ntuser creados en los contextos de por monitor V2 se escalarán en un modo por monitor.
-   **Escalado de cuadros de diálogo** : los cuadros de diálogo de Win32 creados en los contextos de por monitor V2 responderán automáticamente a los cambios de PPP.
-   **Escalado mejorado de los controles comctl32** : varios controles comctl32 tienen un comportamiento de escalado de PPP mejorado en contextos de por monitor V2.
-   **Comportamiento mejorado** : los identificadores de uxtheme abiertos en el contexto de una ventana por monitor V2 funcionarán en función de los PPP asociados a esa ventana.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI no es consciente de la mejora de la calidad del contenido basado en GDI. Este modo se comporta de forma similar a DPI_AWARENESS_CONTEXT_UNAWARE, pero también permite al sistema mejorar automáticamente la calidad de representación de texto y otras primitivas basadas en GDI cuando la ventana se muestra en un monitor de alta ppp.

Para obtener más información, consulte [mejorar la experiencia de PPP alta en aplicaciones de escritorio basadas en GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED se presentó en la actualización de octubre de 2018 de Windows 10 (también conocida como versión 1809).


## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----|-----------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1607 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno <br/>  |
| Encabezado<br/>                   | <dl> <dt>WINDEF. h</dt> </dl> |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AreDpiAwarenessContextsEqual**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**GetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**GetWindowDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**IsValidDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
