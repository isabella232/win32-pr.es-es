---
description: La clase CBaseWindow es una clase base para administrar ventanas.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: Clase CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 313f1b222f3b0096d3f5bf92c15e2097afb29848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661415"
---
# <a name="cbasewindow-class"></a>Clase CBaseWindow

La `CBaseWindow` clase es una clase base para administrar ventanas. Los representadores de vídeo pueden utilizar esta clase para crear ventanas de vídeo. Para usar esta clase, cree una clase derivada que herede de `CBaseWindow` . En la clase derivada:

-   Implemente el método virtual puro [**CBaseWindow:: GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md), que define los estilos de ventana.
-   Invalide el método [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) , que controla los mensajes de ventana.
-   Implemente un destructor que llame al método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) .

Antes de usar una instancia de la clase derivada, llame al método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) .



| Variables de miembro protegidas                                           | Descripción                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**hInstance de m \_**](cbasewindow-m-hinstance.md)                      | Identificador de la instancia de módulo.                                                 |
| [**m \_ hWnd**](cbasewindow-m-hwnd.md)                                | Identificador de la ventana del objeto.                                                 |
| [**m \_ HDC**](cbasewindow-m-hdc.md)                                  | Identificador del contexto de dispositivo de la ventana.                                         |
| [**\_ancho m**](cbasewindow-m-width.md)                              | Ancho del área cliente, en píxeles.                                           |
| [**\_altura m**](cbasewindow-m-height.md)                            | Alto del área cliente, en píxeles.                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | Marca que especifica si se ha activado la ventana.                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | Cadena estática que contiene el nombre de la clase de ventana.                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | Estilos de clase para la ventana.                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | Estilos de ventana para la ventana.                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | Estilos de ventana extendidos para la ventana.                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | Mensaje privado que coloca la ventana en primer plano.                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | Mensaje privado que establece el estilo de ventana en WS \_ ex \_ nivel superior.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Mensaje privado que observa la paleta.                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | Identificador del contexto de dispositivo de memoria.                                           |
| [**m \_ hPalette**](cbasewindow-m-hpalette.md)                        | Identificador de la paleta de la ventana.                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | Marca que especifica si la ventana debe obtener su paleta.             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | Marca que especifica si la paleta debe ser una paleta de fondo.        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | Marca que especifica si se está llevando a cabo una nueva paleta.                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | Sección crítica para serializar el acceso al objeto.                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | Marca que especifica si se debe recuperar el contexto del dispositivo.                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | Marca que especifica si la ventana envía o envía su mensaje de destrucción. |
| Métodos protegidos                                                    | Descripción                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Controla los mensajes de cambio de paleta. Virtualiza.                                      |
| Métodos públicos                                                       | Descripción                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | Método de constructor.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Destruye la ventana. Virtualiza.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Crea la ventana. Virtualiza.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Desactiva la ventana. Virtualiza.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Ajusta el tamaño de la ventana según los requisitos de la clase derivada. Virtualiza.  |
| [**Tamaño**](cbasewindow-onsize.md)                                 | Controla \_ los mensajes de tamaño de WM. Virtualiza.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Controla \_ los mensajes de cierre de WM. Virtualiza.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Recupera el tamaño predeterminado del área cliente. Virtualiza.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Libera los recursos de la ventana. Virtualiza.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Inicializa la ventana. Virtualiza.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Notifica a la ventana que se ha conectado el PIN de entrada del representador.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Crea la ventana.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Alinea la ventana con un límite **DWORD** para obtener el máximo rendimiento.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Establece el estado de presentación de la ventana.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Hace que se vuelva a dibujar la ventana.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Pone la ventana en primer plano.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Instala una paleta para la ventana. Virtualiza.                                    |
| [**SetRealize**](cbasewindow-setrealize.md)                         | Especifica si la ventana obtiene las paletas.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Obtiene la paleta actual de la ventana. Virtualiza.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Permite a una clase derivada reenviar mensajes a otra ventana. Virtualiza.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Recupera el ancho actual de la ventana.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Recupera el alto actual de la ventana.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Recupera un identificador de la ventana.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Recupera un identificador para el contexto de dispositivo de memoria.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Recupera un identificador del contexto de dispositivo de la ventana.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Controla los mensajes de ventana. Virtualiza.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Elimina la paleta actual de la ventana y restaura la paleta predeterminada del sistema.  |
| Métodos virtuales puros                                                 | Descripción                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Recupera los estilos de clase y los estilos de ventana de la ventana.                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




