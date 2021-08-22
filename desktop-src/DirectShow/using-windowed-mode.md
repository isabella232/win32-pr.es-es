---
description: Uso del modo de ventana
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Uso del modo de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f71bfa58e46ade8c779e562278f908c8b8fd593989ed4007e6b98cb7916da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633095"
---
# <a name="using-windowed-mode"></a>Uso del modo de ventana

> [!Note]  
> El filtro de [representador de vídeo heredado](video-renderer-filter.md) siempre usa el modo de ventana. Los filtros VMR-7 y VMR-9 usan el modo de ventana de forma predeterminada, pero también admiten el modo sin ventanas.

 

En modo de ventana, el representador de vídeo crea su propia ventana donde pinta los fotogramas de vídeo. A menos que especifique lo contrario, esta ventana es una ventana de nivel superior con sus propios bordes y barra de título. La mayoría de las veces, sin embargo, adjuntará la ventana de vídeo a una ventana de aplicación para que el vídeo se integre en la interfaz de usuario de la aplicación. Para ello, siga estos pasos:

1.  Consulta de **IVideoWindow**.
2.  Establezca la ventana primaria.
3.  Establecer nuevos estilos de ventana.
4.  Coloque la ventana de vídeo dentro de la ventana del propietario.
5.  Notifique a la ventana de vídeo los mensajes \_ DE WM MOVE.

**Consulta de IVideoWindow**

Antes de iniciar la reproducción, consulte filter Graph Manager para la **interfaz IVideoWindow:**


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Establecer la ventana primaria**

Para establecer la ventana primaria, llame al [**método IVideoWindow::p ut \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un identificador para la ventana de la aplicación. Este método toma una variable de tipo [**OAHWND,**](oahwnd.md)por lo que convierte el identificador a este tipo:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Establecer nuevos estilos de ventana**

Cambie el estilo de la ventana de vídeo llamando al [**método IVideoWindow::p ut \_ WindowStyle:**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle)


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



La marca WS CHILD establece que la ventana sea una ventana secundaria y la marca CLIPSIBLINGS de WS impide que la ventana se dibujo dentro del área de cliente de \_ \_ otra ventana secundaria.

**Posición de la ventana de vídeo**

Para establecer la posición del vídeo en relación con el área cliente de la ventana de aplicación, llame al [**método IVideoWindow::SetWindowPosition.**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) Este método toma un rectángulo que especifica el borde izquierdo, el borde superior, el ancho y el alto de la ventana de vídeo. Por ejemplo, el código siguiente ajusta la ventana de vídeo para ajustarse a todo el área de cliente de la ventana primaria:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Para obtener el tamaño nativo del vídeo, llame al método [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) en filter Graph Manager. Puede usar esa información para escalar el vídeo y mantener la relación de aspecto correcta.

**Responder a mensajes MOVE de WM \_**

Para obtener el mejor rendimiento, debe notificar al representador de vídeo cada vez que la ventana se mueva mientras el gráfico está en pausa. Llame al [**método IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) para reenviar el mensaje \_ MOVE de WM:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Si el representador usa una superposición de hardware, esta notificación hace que el representador actualice la posición de superposición. (VMR-9 no usa superposiciones, por lo que no es necesario llamar a este método si usa VMR-9).

**Limpieza**

Antes de que se cierre la aplicación, detenga el gráfico y restablezca el propietario de la ventana de vídeo a **NULL.** De lo contrario, los mensajes de ventana podrían enviarse a la ventana incorrecta, lo que probablemente provocará errores. Además, oculte la ventana de vídeo o, de lo contrario, podría ver un parpadeo de imágenes de vídeo en la pantalla momentáneamente:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Si el elemento primario de la ventana de vídeo es un elemento secundario de la ventana principal de la aplicación (es decir, si la ventana de vídeo es un elemento secundario de un elemento secundario), debe crear la ventana de vídeo mediante **CoCreateInstance** y agregarla al gráfico, en lugar de permitir que el Administrador de filtros de Graph agregue el representador de vídeo durante [Intelligent Conectar](intelligent-connect.md). Esto garantiza que la ventana de vídeo y la ventana secundaria se vuelvan a dibujar al mismo tiempo. De lo contrario, la ventana secundaria puede pintar sobre la ventana de vídeo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 



