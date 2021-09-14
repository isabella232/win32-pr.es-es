---
description: La clase CBaseWindow es una clase base para administrar ventanas.
ms.assetid: 212d179e-5b5e-49fb-bf0a-a12e0317c96a
title: CBaseWindow (clase, Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973904"
---
# <a name="cbasewindow-class"></a>CBaseWindow (clase)

La `CBaseWindow` clase es una clase base para administrar ventanas. Los representadores de vídeo pueden usar esta clase para crear ventanas de vídeo. Para usar esta clase, cree una clase derivada que herede de `CBaseWindow` . En la clase derivada:

-   Implemente el método virtual [**puro CBaseWindow::GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md), que define los estilos de ventana.
-   Invalide [**el método CBaseWindow::OnReceiveMessage,**](cbasewindow-onreceivemessage.md) que controla los mensajes de ventana.
-   Implemente un destructor que llame al [**método CBaseWindow::D oneWithWindow.**](cbasewindow-donewithwindow.md)

Antes de usar una instancia de la clase derivada, llame al método [**CBaseWindow::P repareWindow.**](cbasewindow-preparewindow.md)



| Variables de miembro protegido                                           | Descripción                                                                    |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**m \_ hInstance**](cbasewindow-m-hinstance.md)                      | Identificador de la instancia del módulo.                                                 |
| [**m \_ hwnd**](cbasewindow-m-hwnd.md)                                | Identificador de la ventana del objeto.                                                 |
| [**m \_ hdc**](cbasewindow-m-hdc.md)                                  | Controlar el contexto del dispositivo de la ventana.                                         |
| [**m \_ Width**](cbasewindow-m-width.md)                              | Ancho del área de cliente, en píxeles.                                           |
| [**m \_ Height**](cbasewindow-m-height.md)                            | Alto del área de cliente, en píxeles.                                          |
| [**m \_ bActivated**](cbasewindow-m-bactivated.md)                    | Marca que especifica si se ha activado la ventana.                     |
| [**m \_ pClassName**](cbasewindow-m-pclassname.md)                    | Cadena estática que contiene el nombre de la clase de ventana.                      |
| [**m \_ ClassStyles**](cbasewindow-m-classstyles.md)                  | Estilos de clase para la ventana.                                                   |
| [**m \_ WindowStyles**](cbasewindow-m-windowstyles.md)                | Estilos de ventana de la ventana.                                                  |
| [**m \_ WindowStylesEx**](cbasewindow-m-windowstylesex.md)            | Estilos de ventana extendidos para la ventana.                                         |
| [**m \_ ShowStageMessage**](cbasewindow-m-showstagemessage.md)        | Mensaje privado que lleva la ventana al primer plano.                      |
| [**m \_ ShowStageTop**](cbasewindow-m-showstagetop.md)                | Mensaje privado que establece el estilo de ventana en WS \_ EX \_ TOPMOST.                 |
| [**m \_ RealizePalette**](cbasewindow-m-realizepalette.md)            | Mensaje privado que realiza la paleta.                                     |
| [**m \_ MemoryDC**](cbasewindow-m-memorydc.md)                        | Controlar el contexto del dispositivo de memoria.                                           |
| [**m \_ hPalette**](cbasewindow-m-hpalette.md)                        | Identificador de la paleta de la ventana.                                                |
| [**m \_ bNoRealize**](cbasewindow-m-bnorealize.md)                    | Marca que especifica si la ventana debe realizar su paleta.             |
| [**m \_ bBackground**](cbasewindow-m-bbackground.md)                  | Marca que especifica si la paleta debe ser una paleta de fondo.        |
| [**m \_ bRealizing**](cbasewindow-m-brealizing.md)                    | Marca que especifica si se va a realizar una nueva paleta.                   |
| [**m \_ WindowLock**](cbasewindow-m-windowlock.md)                    | Sección crítica, para serializar el acceso al objeto .                           |
| [**m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md)                        | Marca que especifica si se debe recuperar el contexto del dispositivo.                    |
| [**m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md)        | Marca que especifica si la ventana publica o envía su mensaje de destrucción. |
| Métodos protegidos                                                    | Descripción                                                                    |
| [**OnPaletteChange**](cbasewindow-onpalettechange.md)               | Controla los mensajes de cambio de paleta. Virtual.                                      |
| Métodos públicos                                                       | Descripción                                                                    |
| [**CBaseWindow**](cbasewindow-cbasewindow.md)                       | Método constructor.                                                            |
| [**DoneWithWindow**](cbasewindow-donewithwindow.md)                 | Destruye la ventana. Virtual.                                                  |
| [**PrepareWindow**](cbasewindow-preparewindow.md)                   | Crea la ventana. Virtual.                                                   |
| [**InactivateWindow**](cbasewindow-inactivatewindow.md)             | Desactiva la ventana. Virtual.                                               |
| [**ActivateWindow**](cbasewindow-activatewindow.md)                 | Tamaños de la ventana según los requisitos de la clase derivada. Virtual.  |
| [**OnSize**](cbasewindow-onsize.md)                                 | Controla los mensajes \_ WM SIZE. Virtual.                                            |
| [**OnClose**](cbasewindow-onclose.md)                               | Controla los mensajes \_ WM CLOSE. Virtual.                                           |
| [**GetDefaultRect**](cbasewindow-getdefaultrect.md)                 | Recupera el tamaño predeterminado del área de cliente. Virtual.                        |
| [**UninitialiseWindow**](cbasewindow-uninitialisewindow.md)         | Libera los recursos de la ventana. Virtual.                                      |
| [**InitialiseWindow**](cbasewindow-initialisewindow.md)             | Inicializa la ventana. Virtual.                                               |
| [**CompleteConnect**](cbasewindow-completeconnect.md)               | Notifica a la ventana que el pin de entrada del representador se ha conectado.          |
| [**DoCreateWindow**](cbasewindow-docreatewindow.md)                 | Crea la ventana.                                                            |
| [**PerformanceAlignWindow**](cbasewindow-performancealignwindow.md) | Alinea la ventana con un límite **DWORD** para obtener el máximo rendimiento.            |
| [**DoShowWindow**](cbasewindow-doshowwindow.md)                     | Establece el estado de presentación de la ventana.                                                  |
| [**PaintWindow**](cbasewindow-paintwindow.md)                       | Hace que se vuelva a dibujar la ventana.                                             |
| [**DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md)   | Lleva la ventana al primer plano.                                           |
| [**SetPalette**](cbasewindow-setpalette.md)                         | Instala una paleta para la ventana. Virtual.                                    |
| [**SetRealize**](cbasewindow-setrealize.md)                         | Especifica si la ventana realiza paletas.                                |
| [**DoRealisePalette**](cbasewindow-dorealisepalette.md)             | Realiza la paleta actual de la ventana. Virtual.                                |
| [**PossiblyEatMessage**](cbasewindow-possiblyeatmessage.md)         | Permite que una clase derivada reenvía mensajes a otra ventana. Virtual.        |
| [**GetWindowWidth**](cbasewindow-getwindowwidth.md)                 | Recupera el ancho actual de la ventana.                                     |
| [**GetWindowHeight**](cbasewindow-getwindowheight.md)               | Recupera el alto actual de la ventana.                                    |
| [**GetWindowHWND**](cbasewindow-getwindowhwnd.md)                   | Recupera un identificador de la ventana.                                              |
| [**GetMemoryHDC**](cbasewindow-getmemoryhdc.md)                     | Recupera un identificador en el contexto del dispositivo de memoria.                               |
| [**GetWindowHDC**](cbasewindow-getwindowhdc.md)                     | Recupera un identificador en el contexto del dispositivo de la ventana.                             |
| [**OnReceiveMessage**](cbasewindow-onreceivemessage.md)             | Controla los mensajes de ventana. Virtual.                                              |
| [**UnsetPalette**](cbasewindow-unsetpalette.md)                     | Elimina la paleta actual de la ventana y restaura la paleta del sistema predeterminada.  |
| Métodos virtuales puros                                                 | Descripción                                                                    |
| [**GetClassWindowStyles**](cbasewindow-getclasswindowstyles.md)     | Recupera los estilos de clase y los estilos de ventana de la ventana.                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




