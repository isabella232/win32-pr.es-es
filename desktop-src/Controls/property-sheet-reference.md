---
title: Hoja de propiedades
description: Esta sección contiene información sobre los elementos de programación utilizados con hojas de propiedades.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50661ece6985c16f299b514fa59068bf06f115b49c0f0bbea783cf637c2c921
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826035"
---
# <a name="property-sheet"></a>Hoja de propiedades

Esta sección contiene información sobre los elementos de programación utilizados con hojas de propiedades.

### <a name="overviews"></a>Temas de introducción



| Tema                                              | Contenido                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Acerca de las hojas de propiedades](property-sheets.md)       | Una *hoja de* propiedades es una ventana que permite al usuario ver y editar las propiedades de un elemento.<br/>                  |
| [Crear asistentes](wizards.md)                    | Un asistente es un tipo de hoja de propiedades que proporciona una manera sencilla y eficaz de guiar a los usuarios a través de un procedimiento.<br/> |
| [Usar hojas de propiedades](using-property-sheets.md) | En esta sección se proporciona información de implementación y código de ejemplo para trabajar con hojas de propiedades.<br/>                     |



 

### <a name="functions"></a>Functions



| Tema                                                        | Contenido                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Especifica una función de devolución de llamada definida por la aplicación que usa una extensión de hoja de propiedades para agregar una página a una hoja de propiedades.<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Crea una nueva página para una hoja de propiedades.<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Destruye una página de hoja de propiedades. Una aplicación debe llamar a esta función para las páginas que no se han pasado a la [**función PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)<br/>                                                                              |
| [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Crea una hoja de propiedades y agrega las páginas definidas en la estructura de encabezados de hoja de propiedades especificada.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Especifica una función de devolución de llamada definida por la aplicación a la que llama una hoja de propiedades cuando se crea una página y cuando está a punto de destruirse. Una aplicación puede usar esta función para realizar operaciones de inicialización y limpieza para la página.<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Función de devolución de llamada definida por la aplicación a la que el sistema llama cuando se crea e inicializa la hoja de propiedades.<br/>                                                                                                                        |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                               | Contenido                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PSM \_ ADDPAGE**](psm-addpage.md)                                 | Agrega una nueva página al final de una hoja de propiedades existente. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet AddPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage)<br/>                                                                                                |
| [**PSM \_ APPLY**](psm-apply.md)                                     | Simula la selección del **botón** Aplicar, lo que indica que una o varias páginas han cambiado y que los cambios deben validarse y grabarse.<br/>                                                                                                                   |
| [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md)                     | Enviado por una aplicación cuando ha realizado cambios desde la notificación APPLY de [PSN \_ más](psn-apply.md) reciente que no se puede cancelar. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ CancelToClose.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose)<br/> |
| [**PSM \_ CAMBIADO**](psm-changed.md)                                 | Informa a una hoja de propiedades de que la información de una página ha cambiado. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ Changed.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed)<br/>                                                                                         |
| [**PSM \_ ENABLEWIZBUTTONS**](psm-enablewizbuttons.md)               | Habilita o deshabilita cualquiera de los botones estándar en un asistente de Aero. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ EnableWizButtons.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons)<br/>                                                                          |
| [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md)           | Recupera un identificador en la ventana de la página actual de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet GetCurrentPageHwnd.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd)<br/>                                                          |
| [**PSM \_ GETRESULT**](psm-getresult.md)                             | Usado por hojas de propiedades modeless para recuperar la información devuelta a las hojas de propiedades modales [**por PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Puede enviar este mensaje explícitamente o usar la macro [**\_ PropSheet GetResult.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)<br/>                 |
| [**PSM \_ GETTABCONTROL**](psm-gettabcontrol.md)                     | Recupera el identificador del control de ficha de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet GetTabControl.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol)<br/>                                                                                 |
| [**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)                         | Toma el identificador de ventana de la página de la hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la [**macro PropSheet \_ HwndToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex)<br/>                                                                  |
| [**PSM \_ IDTOINDEX**](psm-idtoindex.md)                             | Toma el identificador de recurso de una página de hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet IdToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex)<br/>                                                                          |
| [**PSM \_ INDEXTOHWND**](psm-indextohwnd.md)                         | Toma el índice de una página de hoja de propiedades y devuelve su identificador de ventana. Puede enviar este mensaje explícitamente o usar la [**macro PropSheet \_ IndexToHwnd.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd)<br/>                                                                               |
| [**PSM \_ INDEXTOID**](psm-indextoid.md)                             | Toma el índice de una página de hoja de propiedades y devuelve su identificador de recurso. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet IndexToId.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid)<br/>                                                                                     |
| [**PSM \_ INDEXTOPAGE**](psm-indextopage.md)                         | Toma el índice de una página de hoja de propiedades y devuelve su identificador HPROPSHEETPAGE. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet IndexToPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage)<br/>                                                                       |
| [**PSM \_ INSERTPAGE**](psm-insertpage.md)                           | Inserta una nueva página en una hoja de propiedades existente. La página se puede insertar en un índice especificado o después de una página especificada. Puede enviar este mensaje explícitamente o mediante la [**macro \_ PropSheet InsertPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage)<br/>                |
| [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md)                 | Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la [**macro \_ PropSheet IsDialogMessage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage)<br/>                              |
| [**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)                         | Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice de base cero. Puede enviar este mensaje explícitamente o usar la [**macro \_ PropSheet PageToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex)<br/>                                                          |
| [**PSM \_ PRESSBUTTON**](psm-pressbutton.md)                         | Simula la selección de un botón de hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet PressButton.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton)<br/>                                                                                              |
| [**PSM \_ QUERYSIBLINGS**](psm-querysiblings.md)                     | Se envía a una hoja de propiedades, que luego reenvía el mensaje a cada una de sus páginas. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ QuerySiblings.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings)<br/>                                                              |
| [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md)                       | Indica que el sistema debe reiniciarse para que los cambios suban efecto. Puede enviar el mensaje [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) explícitamente o mediante la [**macro PropSheet \_ RebootSystem.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem)<br/>                        |
| [**PSM \_ RECALCPAGESIZES**](psm-recalcpagesizes.md)                 | Vuelve a calcular el tamaño de página de una hoja de propiedades estándar o de asistente después de agregar o quitar páginas. Puede enviar este mensaje explícitamente o usar la [**macro PropSheet \_ RecalcPageSizes.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes)<br/>                                     |
| [**PSM \_ REMOVEPAGE**](psm-removepage.md)                           | Quita una página de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ RemovePage de PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage)<br/>                                                                                                              |
| [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md)                   | Indica que Windows debe reiniciarse para que los cambios suban efecto.<br/>                                                                                                                                                                                         |
| [**PSM \_ SETBUTTONTEXT**](psm-setbuttontext.md)                     | Establece el texto de un botón en un asistente de Aero. Puede enviar este mensaje explícitamente o mediante la [**macro \_ PropSheet SetButtonText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext)<br/>                                                                                                 |
| [**PSM \_ SETCURSEL**](psm-setcursel.md)                             | Activa la página especificada en una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSel.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel)<br/>                                                                                                    |
| [**PSM \_ SETCURSELID**](psm-setcurselid.md)                         | Activa la página dada en una hoja de propiedades basándose en el identificador de recursos de la página. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetCurSelByID.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid)<br/>                                                   |
| [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md)                     | Establece el texto del botón **Finalizar** en un asistente, muestra y habilita el botón y oculta los **botones Siguiente** **y** Atrás. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet SetFinishText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext)<br/>               |
| [**PSM \_ SETHEADERBITMAP**](psm-setheaderbitmap.md)                 | Este mensaje no se implementa.<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERBITMAPRESOURCE**](psm-setheaderbitmapresource.md) | Este mensaje no se implementa.<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERSUBTITLE**](psm-setheadersubtitle.md)             | Establece el texto del subtítulo para el encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o usar la macro [**PropSheet \_ SetHeaderSubTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle)<br/>                                                                        |
| [**PSM \_ SETHEADERTITLE**](psm-setheadertitle.md)                   | Establece el texto del título del encabezado de la página interior de un asistente. Puede enviar este mensaje explícitamente o usar la [**macro PropSheet \_ SetHeaderTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle)<br/>                                                                                 |
| [**PSM \_ SETNEXTTEXT**](psm-setnexttext.md)                         | Establece el texto del botón **Siguiente** en un asistente. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ SetNextText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext)<br/>                                                                                                |
| [**PSM \_ SETTITLE**](psm-settitle.md)                               | Establece el título de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ SetTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle)<br/>                                                                                                                    |
| [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md)                     | Habilita o deshabilita los botones **Atrás,** **Siguiente** **y Finalizar** en un asistente. También puede usar la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para publicar el mensaje.<br/>                                                                          |
| [**PSM \_ SHOWWIZBUTTONS**](psm-showwizbuttons.md)                   | Muestra u oculta los botones de un asistente. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet ShowWizButtons.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons)<br/>                                                                                                        |
| [**PSM \_ SIN CAMBIOS**](psm-unchanged.md)                             | Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado previamente. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ UnChanged.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged)<br/>                                                      |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                     | Contenido                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN \_ APPLY](psn-apply.md)                               | Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, Cerrar o Aplicar y desea que todos los cambios suban efecto. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>      |
| [PSN \_ GETOBJECT](psn-getobject.md)                       | Enviado por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de ficha.<br/>                                                                                                                       |
| [AYUDA \_ DE PSN](psn-help.md)                                 | Notifica a una página que el usuario ha hecho clic en el botón Ayuda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                          |
| [PSN \_ KILLACTIVE](psn-killactive.md)                     | Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha hecho clic en **el botón** Aceptar. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>       |
| [PSN \_ QUERYCANCEL](psn-querycancel.md)                   | Indica que el usuario ha cancelado la hoja de propiedades. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                            |
| [PSN \_ QUERYINITIALFOCUS](psn-queryinitialfocus.md)       | Enviado por una hoja de propiedades para proporcionar una página de hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>           |
| [RESTABLECIMIENTO DE \_ PSN](psn-reset.md)                               | Notifica a una página que la hoja de propiedades está a punto de destruirse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                   |
| [PSN \_ SETACTIVE](psn-setactive.md)                       | Notifica a una página que está a punto de activarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                                   |
| [PSN \_ TRANSLATEACCELERATOR](psn-translateaccelerator.md) | Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado. Proporciona a la página una oportunidad para realizar la traducción del acelerador de teclado privado. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/> |
| [PSN \_ WIZBACK](psn-wizback.md)                           | Notifica a una página que el usuario ha hecho clic en el **botón** Atrás de un asistente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                          |
| [PSN \_ WIZFINISH](psn-wizfinish.md)                       | Notifica a una página que el usuario ha hecho clic en **el botón** Finalizar de un asistente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                        |
| [PSN \_ WIZNEXT](psn-wiznext.md)                           | Notifica a una página que el usuario ha hecho clic en el **botón** Siguiente de un asistente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                          |



 

### <a name="structures"></a>Estructuras



| Tema                                      | Contenido                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Define el marco y las páginas de una hoja de propiedades.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Define una página en una hoja de propiedades.<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Contiene información para los códigos de notificación de la hoja de propiedades.<br/> |



 

 

