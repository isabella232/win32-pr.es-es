---
title: Agregar y modificar eventos
description: Agregar y modificar eventos
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357386"
---
# <a name="adding-and-modifying-the-events"></a>Agregar y modificar eventos

Debe proporcionar controladores de eventos para los eventos de cambio de EN \_ que se producen cuando el usuario cambia el texto en los cuadros de edición de la página de propiedades. Estos controladores de eventos tienen una implementación simple que simplemente permite **aplicar** en el cuadro de diálogo Página de propiedades.

## <a name="modifying-the-scale-factor-event-handler"></a>Modificar el controlador de eventos de factor de escala

Debe cambiar el nombre del controlador de eventos existente que el Asistente para complementos proporcionó para el cuadro de edición del factor de escala. Debe cambiar el nombre de OnChangeScale a OnChangeDelay en tres ubicaciones:

1.  En EchoPropPage. h, cambie el nombre en la sección macro de mapa de mensajes. Reemplace la línea que asigna el evento de cambio de factor de escala al método OnChangeScale por el código siguiente:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  En EchoPropPage. h, cambie el nombre en la línea que cree un prototipo de la función OnChangeScale:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  En EchoPropPage. cpp, cambie el nombre en el encabezado de la función:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Agregar el controlador de eventos de la combinación húmeda

Puede agregar fácilmente el controlador de eventos para el \_ evento en cambio que está asociado al control del \_ cuadro de edición IDC WETMIX. En el editor de recursos del cuadro de diálogo:

1.  Haga clic con el botón derecho en el \_ cuadro de edición IDC WETMIX y elija **eventos**. Aparecerá el cuadro de diálogo nuevo mensaje de Windows y controladores de eventos.
2.  En el cuadro **clase u objeto que se va a administrar** , haga clic en el nombre del recurso del cuadro de edición, IDC \_ WETMIX.
3.  En el cuadro **nuevos mensajes o eventos de Windows** , haga clic en \_ cambiar para seleccionarlo.
4.  Haga clic en **Agregar controlador**. Aparecerá el cuadro de diálogo Agregar función miembro.
5.  En el cuadro Nombre de la **función miembro** , escriba el nombre OnChangeWetmix.
6.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo Agregar función miembro.
7.  Haga clic en **Aceptar** para volver al editor de recursos del cuadro de diálogo.

Visual C++ agrega automáticamente el código para el mapa de mensajes y la función de controlador de eventos a EchoPropPage. h. El código que inserta proporciona un comentario TODO donde puede Agregar la implementación en el encabezado de la función. Se trata de un estilo ligeramente diferente del que usa el código de ejemplo del Asistente para complementos de Windows Media Player, pero es aceptable.

Si desea escribir la implementación en el archivo de encabezado o moverla a EchoPropPage. cpp. En cualquier caso, la implementación solo necesita una línea de código adicional para habilitar **aplicar** en el cuadro de diálogo de la página de propiedades. Inserte esta línea de código antes de la línea que devuelve de la función:


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades de ejemplo echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




