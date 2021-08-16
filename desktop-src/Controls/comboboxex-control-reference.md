---
title: ComboBoxEx Control
description: Esta sección contiene información sobre los elementos de programación utilizados con los controles ComboBoxEx.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded6ff945424f63baaf0063ce5d8897f84883d5063989aa6c7a9fb1a4f76a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413468"
---
# <a name="comboboxex-control"></a>ComboBoxEx Control

Esta sección contiene información sobre los elementos de programación utilizados con los controles ComboBoxEx.

### <a name="overviews"></a>Temas de introducción



| Tema                                                | Contenido                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Acerca de los controles ComboBoxEx](comboboxex-controls.md) | Los controles ComboBoxEx son controles de cuadro combinado que proporcionan compatibilidad nativa con imágenes de elementos.<br/> |
| [Usar controles ComboBoxEx](using-comboboxex.md)    | Esta sección contiene código de ejemplo e información sobre cómo usar controles ComboBoxEx.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                   | Contenido                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | Quita un elemento de un control ComboBoxEx. <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | Obtiene el identificador del control de cuadro combinado secundario. <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el estilo [**DE LISTA DESPLEGABLE \_ de CBS.**](combo-box-styles.md) <br/> |
| [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) | Obtiene los estilos extendidos que se usan para un control ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETIMAGELIST**](cbem-getimagelist.md)         | Obtiene el identificador de una lista de imágenes asignada a un control ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETITEM**](cbem-getitem.md)                   | Obtiene información de elemento para un elemento ComboBoxEx determinado.<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | Obtiene la marca de formato de caracteres UNICODE para el control. <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | Determina si el usuario ha cambiado el texto de un control de edición ComboBoxEx.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Inserta un nuevo elemento en un control ComboBoxEx. <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | Este mensaje no se implementa. <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | Este mensaje no se implementa. <br/>                                                                                                                                                               |
| [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) | Establece estilos extendidos dentro de un control ComboBoxEx. <br/>                                                                                                                                              |
| [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md)         | Establece una lista de imágenes para un control ComboBoxEx. <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | Establece los atributos de un elemento en un control ComboBoxEx. <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | Establece la marca de formato de caracteres UNICODE para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | Establece el estilo visual de un control ComboBoxEx.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                      | Contenido                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | Se envía cuando el usuario activa la lista desplegable o hace clic en el cuadro de edición del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | Se envía cuando se ha eliminado un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                     |
| [DRAGBEGIN DE CBEN \_](cben-dragbegin.md)                      | Se envía cuando el usuario comienza a arrastrar la imagen del elemento que se muestra en la parte de edición del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | Se envía cuando el usuario ha finalizado una operación dentro del cuadro de edición o ha seleccionado un elemento de la lista desplegable del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                             |
| [GETDISPINFO DE CBEN \_](cben-getdispinfo.md)                  | Se envía para recuperar información de visualización sobre un elemento de devolución de llamada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Se envía cuando se ha insertado un nuevo elemento en el control . Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                  |
| [NM \_ SETCURSOR (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Notifica a la ventana primaria de un control ComboBoxEx que el control establece el cursor en respuesta a un [**mensaje \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) de WM. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

### <a name="structures"></a>Estructuras



| Tema                                    | Contenido                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Contiene información sobre un elemento de un control ComboBoxEx.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Contiene información usada con el código [de notificación \_ DRAGBEGIN de CBEN.](cben-dragbegin.md) <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Contiene información sobre la conclusión de una operación de edición dentro de un control ComboBoxEx. Esta estructura se usa con el código [de notificación \_ ENDEDIT de CBEN.](cben-endedit.md) <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Contiene información específica de los elementos ComboBoxEx para su uso con códigos de notificación. <br/>                                                                                               |



 

### <a name="constants"></a>Constantes



| Tema                                                                        | Contenido                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Estilos extendidos del control ComboBoxEx](comboboxex-control-extended-styles.md) | Admite los estilos extendidos que aparecen en esta sección, así como la mayoría de los estilos de control de cuadro combinado estándar.<br/> |



 

 

