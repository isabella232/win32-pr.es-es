---
title: DPI_AWARENESS_CONTEXT identificador (windef.h)
description: Identifica el contexto de reconocimiento de una ventana.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575001"
---
# <a name="dpi_awareness_context-handle"></a>Identificador DE \_ CONTEXTO DE RECONOCIMIENTO DE \_ PPP

Identifica el contexto de reconocimiento de una ventana.

## <a name="syntax"></a>Sintaxis

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Constantes

**CONTEXTO DE \_ RECONOCIMIENTO DE PPP SIN \_ \_ RECONOCIMIENTO**<dl> PPP sin reconocimiento. Esta ventana no se escala para los cambios de PPP y siempre se supone que tiene un factor de escala del 100 % (96 PPP). El sistema lo escalará automáticamente en cualquier otra configuración de PPP.  
</dl>

**RECONOCIMIENTO DEL \_ SISTEMA DE CONTEXTO DE RECONOCIMIENTO DE \_ \_ \_ PPP**<dl> Compatible con PPP del sistema. Esta ventana no se escala para los cambios de PPP. Consultará el valor de PPP una vez y usará ese valor durante la vigencia del proceso. Si cambia el valor de PPP, el proceso no se ajustará al nuevo valor de PPP. El sistema lo escalará o reducirá verticalmente automáticamente cuando cambie el valor de PPP desde el valor del sistema.  
</dl>

**CONTEXTO DE \_ RECONOCIMIENTO DE PPP POR MONITOR \_ \_ \_ \_ COMPATIBLE**<dl> Compatible con PPP por monitor. Esta ventana comprueba el valor de PPP cuando se crea y ajusta el factor de escala cada vez que cambia el valor de PPP. El sistema no escala automáticamente estos procesos.  
</dl>

**CONTEXTO DE \_ RECONOCIMIENTO DE PPP POR MONITOR COMPATIBLE CON \_ \_ \_ \_ \_ V2**<dl> También se conoce como **Por monitor v2.** Un avance sobre el modo de reconocimiento de PPP por monitor original, que permite a las aplicaciones acceder a nuevos comportamientos de escalado relacionados con PPP en cada ventana de nivel superior.  
Per Monitor v2 estaba disponible en Creators Update de Windows 10 y no está disponible en versiones anteriores del sistema operativo.  
Los comportamientos adicionales introducidos son los siguientes:

-   **Notificaciones de cambio de PPP de** la ventana secundaria: en contextos por monitor v2, se notifica a todo el árbol de ventana los cambios de PPP que se produzcan.
-   **Escalado del área que no es** cliente: todas las ventanas tendrán automáticamente su área no cliente dibujada de forma confidencial con PPP. Las llamadas [**a EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) no son necesarias.
-   **Escalado de menús Win32:** todos los menús NTUSER creados en los contextos de Per Monitor v2 se escalarán de forma por monitor.
-   **Escalado de diálogos:** los cuadros de diálogo win32 creados en contextos por monitor v2 responderán automáticamente a los cambios de PPP.
-   **Escalado mejorado de controles comctl32:** varios controles comctl32 han mejorado el comportamiento de escalado de PPP en contextos por monitor v2.
-   **Comportamiento de la cuestión** mejorado: los identificadores de UxTheme abiertos en el contexto de una ventana por monitor v2 funcionarán en términos de ppp asociados a esa ventana.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

PPP sin reconocimiento con una calidad mejorada del contenido basado en GDI. Este modo se comporta de forma similar a DPI_AWARENESS_CONTEXT_UNAWARE, pero también permite al sistema mejorar automáticamente la calidad de representación del texto y otras primitivas basadas en GDI cuando la ventana se muestra en un monitor de valores altos de PPP.

Para obtener más información, consulte [Improving the high-PPP experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97)(Mejora de la experiencia de valores altos de PPP en aplicaciones de escritorio basadas en GDI).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED se introdujo en la actualización de octubre de 2018 de Windows 10 (también conocida como versión 1809).


## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----|-----------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1607 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno <br/>  |
| Encabezado<br/>                   | <dl> <dt>windef.h</dt> </dl> |

## <a name="see-also"></a>Consulte también

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
