---
title: Agregar y modificar los eventos
description: Agregar y modificar los eventos
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos de DSP, páginas de propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 464d20b600a5535e3cf2c02be01fa19c10a590e143c7a96375580719b70c274c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865345"
---
# <a name="adding-and-modifying-the-events"></a>Agregar y modificar los eventos

Debe proporcionar controladores de eventos para los eventos EN CHANGE que se producen cuando el usuario cambia el texto en los cuadros de edición \_ de la página de propiedades. Estos controladores de eventos tienen una implementación sencilla que simplemente habilita **Aplicar en** el cuadro de diálogo de la página de propiedades.

## <a name="modifying-the-scale-factor-event-handler"></a>Modificar el controlador de eventos de Factor de escala

Debe cambiar el nombre del controlador de eventos existente que proporcionó el asistente para complementos para el cuadro de edición del factor de escala. Debe cambiar el nombre de OnChangeScale a OnChangeDelay en tres ubicaciones:

1.  En EchoPropPage.h, cambie el nombre en la sección de macro del mapa de mensajes. Reemplace la línea que asigna el evento de cambio de factor de escala al método OnChangeScale por el código siguiente:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  En EchoPropPage.h, cambie el nombre de la línea que prototipos de la función OnChangeScale:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  En EchoPropPage.cpp, cambie el nombre en el encabezado de función:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Adición del controlador de eventos de mezcla con mezcla con humedad

Puede agregar fácilmente el controlador de eventos para el evento EN CHANGE que está asociado al control de cuadro de edición \_ \_ IDC WETMIX. En el editor de recursos del cuadro de diálogo:

1.  Haga clic con el botón derecho en el cuadro de edición \_ IDC WETMIX y elija **Eventos**. Aparece el cuadro Windows cuadro de diálogo Nuevos controladores de eventos y mensajes.
2.  En el **cuadro Clase u objeto que se debe controlar,** haga clic en el nombre del recurso del cuadro de edición, IDC \_ WETMIX.
3.  En el **cuadro Windows mensajes y eventos,** haga clic en EN CAMBIAR para \_ seleccionarlo.
4.  Haga clic **en Agregar controlador**. Aparece el cuadro de diálogo Agregar función miembro .
5.  En el **cuadro Nombre de función** miembro, escriba el nombre OnChangeWetmix.
6.  Haga **clic en** Aceptar para cerrar el cuadro de diálogo Agregar función miembro .
7.  Haga **clic en** Aceptar para volver al editor de recursos del cuadro de diálogo.

Visual C++ agrega automáticamente el código para la asignación de mensajes y para la función de controlador de eventos a EchoPropPage.h. El código que inserta proporciona un comentario TODO donde puede agregar la implementación en el encabezado de la función. Se trata de un estilo ligeramente diferente al que usa el Reproductor de Windows Media ejemplo del Asistente para complementos, pero es aceptable.

Si desea escribir la implementación en el archivo de encabezado o moverla a EchoPropPage.cpp, usted es su equipo. En cualquier caso, la implementación solo necesita una sola línea de código adicional para habilitar **Aplicar en** el cuadro de diálogo de la página de propiedades. Inserte esta línea de código antes de la línea que devuelve de la función :


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




