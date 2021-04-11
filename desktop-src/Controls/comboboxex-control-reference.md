---
title: Control ComboBoxEx
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles ComboBoxEx.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d5a926ccf2f9f5b5bb68e040731d6b9d8e37ee8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003581"
---
# <a name="comboboxex-control"></a>Control ComboBoxEx

Esta sección contiene información sobre los elementos de programación que se utilizan con los controles ComboBoxEx.

### <a name="overviews"></a>Temas de introducción



| Tema                                                | Contenido                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Acerca de los controles ComboBoxEx](comboboxex-controls.md) | Los controles ComboBoxEx son controles de cuadro combinado que proporcionan compatibilidad nativa con imágenes de elementos.<br/> |
| [Usar controles ComboBoxEx](using-comboboxex.md)    | Esta sección contiene código de ejemplo e información sobre cómo usar los controles ComboBoxEx.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                   | Contenido                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | Quita un elemento de un control ComboBoxEx. <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | Obtiene el identificador del control de cuadro combinado secundario. <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el estilo de [**\_ lista desplegable CBS**](combo-box-styles.md) . <br/> |
| [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) | Obtiene los estilos extendidos que se usan para un control ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETIMAGELIST**](cbem-getimagelist.md)         | Obtiene el identificador de una lista de imágenes asignada a un control ComboBoxEx. <br/>                                                                                                                             |
| [**\_GETITEM CBEM**](cbem-getitem.md)                   | Obtiene la información de un elemento ComboBoxEx determinado.<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | Obtiene la marca del formato de caracteres Unicode para el control. <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Inserta un nuevo elemento en un control ComboBoxEx. <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | Este mensaje no está implementado. <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | Este mensaje no está implementado. <br/>                                                                                                                                                               |
| [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) | Establece los estilos extendidos dentro de un control ComboBoxEx. <br/>                                                                                                                                              |
| [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md)         | Establece una lista de imágenes para un control ComboBoxEx. <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | Establece los atributos de un elemento en un control ComboBoxEx. <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | Establece la marca del formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | Establece el estilo visual de un control ComboBoxEx.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                      | Contenido                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | Se envía cuando el usuario activa la lista desplegable o hace clic en el cuadro de edición del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | Se envía cuando se ha eliminado un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                     |
| [CBEN \_ DRAGBEGIN](cben-dragbegin.md)                      | Se envía cuando el usuario comienza a arrastrar la imagen del elemento mostrado en la parte de edición del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | Se envía cuando el usuario ha finalizado una operación en el cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                             |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md)                  | Se envía para recuperar información de visualización sobre un elemento de devolución de llamada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Se envía cuando se inserta un nuevo elemento en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                  |
| [NM \_ SETCURSOR (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Notifica a la ventana primaria de un control ComboBoxEx que el control está estableciendo el cursor en respuesta a un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Estructuras



| Tema                                    | Contenido                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Contiene información sobre un elemento en un control ComboBoxEx.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Contiene información que se usa con el código de notificación [ \_ DRAGBEGIN de CBEN](cben-dragbegin.md) . <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Contiene información sobre la finalización de una operación de edición en un control ComboBoxEx. Esta estructura se usa con el código de notificación [CBEN \_ ENDEDIT](cben-endedit.md) . <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Contiene información específica de los elementos ComboBoxEx para su uso con códigos de notificación. <br/>                                                                                               |



 

### <a name="constants"></a>Constantes



| Tema                                                                        | Contenido                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Estilos extendidos del control ComboBoxEx](comboboxex-control-extended-styles.md) | Admite los estilos extendidos que se enumeran en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.<br/> |



 

 

