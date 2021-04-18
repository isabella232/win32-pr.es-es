---
description: Usar el modo de ventana
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Usar el modo de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667847"
---
# <a name="using-windowed-mode"></a>Usar el modo de ventana

> [!Note]  
> El [filtro de representador de vídeo](video-renderer-filter.md) heredado siempre usa el modo de ventana. Los filtros VMR-7 y VMR-9 usan el modo de ventana de forma predeterminada, pero también admiten el modo sin ventanas.

 

En el modo de ventana, el representador de vídeo crea su propia ventana donde pinta los fotogramas de vídeo. A menos que especifique lo contrario, esta ventana es una ventana de nivel superior con sus propios bordes y barra de título. Sin embargo, la mayoría de las veces se adjuntará la ventana de vídeo a una ventana de la aplicación, de modo que el vídeo se integre en la interfaz de usuario de la aplicación. Para ello, siga estos pasos:

1.  Consulta para **IVideoWindow**.
2.  Establezca la ventana primaria.
3.  Establecer nuevos estilos de ventana.
4.  Coloque la ventana de vídeo dentro de la ventana propietaria.
5.  Notifique a la ventana de vídeo de \_ los mensajes de movimiento de WM.

**Consulta de IVideoWindow**

Antes de iniciar la reproducción, consulte el administrador de gráficos de filtro para la interfaz **IVideoWindow** :


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Establecer la ventana primaria**

Para establecer la ventana primaria, llame al método [**IVideoWindow::p UT \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un identificador a la ventana de la aplicación. Este método toma una variable de tipo [**OAHWND**](oahwnd.md), por lo que convierta el identificador a este tipo:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Establecer nuevos estilos de ventana**

Cambie el estilo de la ventana de vídeo mediante una llamada al método [**IVideoWindow::p se ha UT \_ estiloVentana**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



La \_ marca WS Child establece que la ventana sea una ventana secundaria y la marca WS \_ CLIPSIBLINGS impide que la ventana dibuje dentro del área cliente de otra ventana secundaria.

**Colocar la ventana de vídeo**

Para establecer la posición del vídeo en relación con el área de cliente de la ventana de la aplicación, llame al método [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) . Este método toma un rectángulo que especifica el borde izquierdo, el borde superior, el ancho y el alto de la ventana de vídeo. Por ejemplo, el código siguiente ajusta la ventana de vídeo para que se ajuste a todo el área cliente de la ventana primaria:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Para obtener el tamaño nativo del vídeo, llame al método [**IBasicVideo:: GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) en el administrador de gráficos de filtro. Puede usar esa información para escalar el vídeo y mantener la relación de aspecto correcta.

**Respuesta a mensajes de movimiento de WM \_**

Para obtener el mejor rendimiento, debe notificar al representador de vídeo cada vez que la ventana se mueva mientras el gráfico esté en pausa. Llame al método [**IVideoWindow:: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) para reenviar el \_ mensaje de movimiento de WM:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Si el representador usa una superposición de hardware, esta notificación hace que el representador actualice la posición de superposición. (VMR-9 no utiliza superposiciones, por lo que no es necesario llamar a este método si se usa VMR-9).

**Limpiar**

Antes de que se cierre la aplicación, detenga el gráfico y restablezca el propietario de la ventana de vídeo en **null**. De lo contrario, es posible que los mensajes de ventana se envíen a una ventana incorrecta, lo que es probable que provoque errores. Además, oculte la ventana de vídeo o, de lo contrario, podría ver una imagen de vídeo parpadeando en la pantalla momentáneamente:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Si el elemento primario de la ventana de vídeo es un elemento secundario de la ventana principal de la aplicación (es decir, si la ventana de vídeo es un elemento secundario de un elemento secundario), debe crear la ventana de vídeo mediante **CoCreateInstance** y agregarla al gráfico, en lugar de permitir que el administrador de gráficos de filtros agregue el representador de vídeo durante la [conexión inteligente](intelligent-connect.md). Esto garantiza que la ventana de vídeo y la ventana secundaria se repintan al mismo tiempo. De lo contrario, la ventana secundaria puede pintar sobre la ventana de vídeo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 



