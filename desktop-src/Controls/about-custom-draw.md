---
title: Acerca del dibujo personalizado
description: Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información general conceptual sobre cómo una aplicación puede admitir el dibujo personalizado.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121a4df5aa6fab222a5c4387ebdcfba51a7977b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968760"
---
# <a name="about-custom-draw"></a>Acerca del dibujo personalizado

Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información general conceptual sobre cómo una aplicación puede admitir el dibujo personalizado. Actualmente, los controles siguientes admiten la funcionalidad de dibujo personalizada:

-   Controles de encabezado
-   Controles de vista de lista
-   Controles Rebar
-   Controles de la barra de herramientas
-   Controles de información sobre herramientas
-   Controles trackbar
-   Controles de vista de árbol

<!-- -->

-   [Acerca de los mensajes de notificación de dibujo personalizados](#about-custom-draw-notification-messages)
-   [Paint Ciclos, etapas de dibujo y mensajes de notificación](#paint-cycles-drawing-stages-and-notification-messages)
-   [Aprovechar los servicios de dibujo personalizados](#taking-advantage-of-custom-draw-services)
    -   [Respuesta a la notificación de prepintado](#responding-to-the-prepaint-notification)
    -   [Solicitud de notificaciones específicas del elemento](#requesting-item-specific-notifications)
    -   [Dibujar el elemento usted mismo](#drawing-the-item-yourself)
    -   [Cambio de fuentes y colores](#changing-fonts-and-colors)
-   [Dibujo personalizado con controles List-View y Tree-View personalizados](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Dibujo personalizado con List-View controles](#custom-draw-with-list-view-controls)
-   [Temas relacionados](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Acerca de los mensajes de notificación de dibujo personalizados

Todos los controles comunes que admiten el dibujo personalizado envían códigos de notificación [ \_ NM CUSTOMDRAW](nm-customdraw.md) en puntos específicos durante las operaciones de dibujo. Estos códigos de notificación describen las operaciones de dibujo que se aplican a todo el control, así como las operaciones de dibujo específicas de los elementos del control. Al igual que muchos códigos de notificación, las notificaciones DE NM \_ CUSTOMDRAW se envían como [**mensajes WM \_ NOTIFY.**](wm-notify.md)

El *parámetro lParam* de una notificación de dibujo personalizada será la dirección de una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) o una estructura específica del control que contiene una estructura **NMCUSTOMDRAW** como su primer miembro. En la tabla siguiente se muestra la relación entre los controles y las estructuras que usan.



| Estructura                                | Usado por                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Controles rebar, trackbar y header |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Controles de vista de lista                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Controles de la barra de herramientas                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Controles de información sobre herramientas                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Controles de vista de árbol                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Paint Ciclos, etapas de dibujo y mensajes de notificación

Al igual que Windows aplicaciones, los controles comunes se pintan y borran periódicamente en función de los mensajes recibidos del sistema u otras aplicaciones. El proceso de dibujo o borrado de un control se denomina ciclo *de pintura.* Los controles que admiten el dibujo personalizado envían [códigos de notificación NM \_ CUSTOMDRAW](nm-customdraw.md) periódicamente a través de cada ciclo de pintura. Este código de notificación va acompañado de una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) u otra estructura que contiene una estructura **NMCUSTOMDRAW** como su primer miembro.

Una parte de la información que contiene [**la estructura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es la fase actual del ciclo de pintura. Esto se conoce como fase *de* dibujo y se representa mediante el valor del miembro **dwDrawStage** de la estructura. Un control informa a su elemento primario de cuatro fases básicas de dibujo. Estas fases de dibujo básicas o globales se representan en la estructura mediante los siguientes valores de marca (definidos en Commctrl.h).



| Valores de fase de dibujo global | Descripción                        |
|--------------------------|------------------------------------|
| PREPINTADO DE CDDS \_           | Antes de que comience el ciclo de pintura.     |
| POSTPAINT de CDDS \_          | Una vez completado el ciclo de pintura. |
| CDDS \_ PREERASE           | Antes de que comience el ciclo de borrado.     |
| PÓSTERASE DE \_ CDDS          | Una vez completado el ciclo de borrado. |



 

Cada uno de los valores anteriores se puede combinar con la marca ITEM de CDDS \_ para especificar las fases de dibujo específicas de los elementos. Para mayor comodidad, Commctrl.h contiene los siguientes valores específicos del elemento.



| Valores de fase de dibujo específicos del elemento | Descripción                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ELEMENTO DE \_ CDDSPREPAINT              | Antes de dibujar un elemento.                                                                                                                                                                                                                                                            |
| ELEMENTO DE \_ CDDSPOSTPAINT             | Después de dibujar un elemento.                                                                                                                                                                                                                                                       |
| ELEMENTO DE \_ CDDSPREERASE              | Antes de borrar un elemento.                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | Una vez borrado un elemento.                                                                                                                                                                                                                                                      |
| SUBELEMENTO DE CDDS \_                   | [Versiones de Common Control](common-control-versions.md) 4.71. Marca combinada con CDDS \_ ITEMPREPAINT o CDDS \_ ITEMPOSTPAINT si se dibuja un subelemento. Esto solo se establecerá si [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) se devuelve desde CDDS \_ PREPAINT. |



 

La aplicación debe procesar el código [de notificación DE NM \_ CUSTOMDRAW](nm-customdraw.md) y, a continuación, devolver un valor específico que informa al control de lo que debe hacer. Consulte las secciones siguientes para obtener más información sobre estos valores devueltos.

## <a name="taking-advantage-of-custom-draw-services"></a>Aprovechar los servicios de dibujo personalizados

La clave para aprovechar la funcionalidad de dibujo personalizada es responder a los códigos de notificación [DE NM \_ CUSTOMDRAW](nm-customdraw.md) que envía un control. Los valores devueltos que la aplicación envía en respuesta a estas notificaciones determinan el comportamiento del control para ese ciclo de pintura.

Esta sección contiene información sobre cómo la aplicación puede usar los valores devueltos de notificación [DE NM \_ CUSTOMDRAW](nm-customdraw.md) para determinar el comportamiento del control.

Los detalles se desglosan en los temas siguientes:

-   [Respuesta a la notificación de prepintado](#responding-to-the-prepaint-notification)
-   [Solicitud de notificaciones específicas del elemento](#requesting-item-specific-notifications)
-   [Dibujar el elemento usted mismo](#drawing-the-item-yourself)
-   [Cambio de fuentes y colores](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Respuesta a la notificación de prepintado

Al principio de cada ciclo de pintura, el control envía el código de notificación [NM \_ CUSTOMDRAW,](nm-customdraw.md) especificando el valor PREPAINT de CDDS en el miembro \_ **dwDrawStage** de la estructura CUSTOMDRAW de NM que lo \_ acompaña. El valor que la aplicación devuelve a esta primera notificación determina cómo y cuándo el control envía notificaciones de dibujo personalizadas posteriores para el resto de ese ciclo de pintura. La aplicación puede devolver una combinación de las marcas siguientes en respuesta a la primera notificación.



| Valor devuelto            | Efecto                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDRF \_ DODEFAULT         | El control se dibujará a sí mismo. No enviará notificaciones [adicionales de NM \_ CUSTOMDRAW](nm-customdraw.md) para este ciclo de pintura. Esta marca no se puede usar con ninguna otra marca.                                                                                                                                                                                                                                                                               |
| CDRF \_ DOERASE           | El control solo dibujará el fondo.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambio de fuentes y colores.](#changing-fonts-and-colors) Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | El control notificará al elemento primario cualquier operación de dibujo específica del elemento. Enviará códigos [de notificación DE NM \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | El control enviará una notificación [NM \_ CUSTOMDRAW](nm-customdraw.md) cuando se complete el ciclo de dibujo de todo el control. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [Versión 4.71.](common-control-versions.md) La aplicación recibirá una notificación [NM \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT CDDS SUBITEM antes de dibujar cada subelemento de \| vista de \_ lista. A continuación, puede especificar la fuente y el color de cada subelemento por separado o devolver [**CDRF \_ DODEFAULT**](cdrf-constants.md) para el procesamiento predeterminado. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT. |
| CDRF \_ SKIPDEFAULT       | La aplicación hizo que el elemento se dibujara manualmente. El control no dibujará el elemento. Esto ocurre cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | El control no dibujará el rectángulo de foco alrededor de un elemento.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Solicitud de notificaciones específicas del elemento

Si la aplicación devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) a la notificación inicial de dibujo personalizado previamente, el control enviará notificaciones para cada elemento que dibuje durante ese ciclo de dibujo. Estas notificaciones específicas del elemento tendrán el valor ITEMPREPAINT de CDDS en el \_ **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que lo acompaña. Puede solicitar que el control envíe otra notificación cuando termine de dibujar el elemento devolviendo [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) a estas notificaciones específicas del elemento. De lo contrario, [**devuelva \_ CDRF DODEFAULT**](cdrf-constants.md) y el control no notificará a la ventana primaria hasta que empiece a dibujar el elemento siguiente.

### <a name="drawing-the-item-yourself"></a>Dibujar el elemento usted mismo

Si la aplicación dibuja todo el elemento, devuelva [**CDRF \_ SKIPDEFAULT.**](cdrf-constants.md) Esto permite que el control omita los elementos que no necesita dibujar, lo que reduce la sobrecarga del sistema. Tenga en cuenta que devolver este valor significa que el control no dibujará ninguna parte del elemento.

### <a name="changing-fonts-and-colors"></a>Cambio de fuentes y colores

La aplicación puede usar el dibujo personalizado para cambiar la fuente de un elemento. Solo tiene que seleccionar el HFONT que desee en el contexto de dispositivo especificado por el **miembro hdc** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada a la notificación de dibujo personalizada. Dado que la fuente que seleccione puede tener métricas diferentes de la fuente predeterminada, asegúrese de incluir el bit [**\_ NEWFONT**](cdrf-constants.md) de CDRF en el valor devuelto del mensaje de notificación. Para obtener más información sobre el uso de esta funcionalidad, vea el código de ejemplo en [Using Custom Draw](using-custom-draw.md). La fuente que especifica la aplicación se usa para mostrar ese elemento cuando no está seleccionado. El dibujo personalizado no permite cambiar los atributos de fuente de los elementos seleccionados.

Para cambiar los colores de texto de todos los controles que admiten el dibujo personalizado, excepto la vista de lista y la vista de árbol, basta con establecer el texto y los colores de fondo deseados en el contexto del dispositivo proporcionado en la estructura de notificación de dibujo personalizada con las funciones [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) y [**SetBkColor.**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) Para modificar los colores de texto en la vista de lista o la vista de árbol, debe colocar los valores de color deseados en los miembros **clrText** y **clrTextBk** de la estructura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) [**o NMTVCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw)

> [!Note]  
> Antes de [la versión 6.0 de](common-control-versions.md) los controles comunes, las barras de herramientas ignoran la marca [**\_ NEWFONT de CDRF.**](cdrf-constants.md) La versión 6.0 admite la marca **\_ NEWFONT de CDRF** y puede usarla para seleccionar una fuente diferente para la barra de herramientas. Sin embargo, no puede cambiar el color de una barra de herramientas cuando un estilo visual está activo. Para cambiar el color de una barra de herramientas en la versión 6.0, primero debe deshabilitar los estilos visuales llamando a [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) y sin especificar ningún estilo visual:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Dibujo personalizado con controles List-View y Tree-View personalizados

Los controles más comunes se pueden controlar básicamente de la misma manera. Sin embargo, los controles list-view y tree-view tienen algunas características que requieren un enfoque ligeramente diferente para el dibujo personalizado.

Para [la versión 5.0,](common-control-versions.md)estos dos controles pueden mostrar texto recortado si cambia la fuente devolviendo [**\_ CDRF NEWFONT**](cdrf-constants.md). Este comportamiento es necesario para la compatibilidad con versiones anteriores de los controles comunes. Si desea cambiar la fuente de un control list-view o tree-view, se obtienen mejores resultados si envía un mensaje [**\_ SETVERSION**](ccm-setversion.md) de CCM con el valor *wParam* establecido en 5 antes de agregar elementos al control. Para obtener un ejemplo de un control de vista de árbol que usa el dibujo personalizado, vea Knowledge Base artículo [SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496).

### <a name="custom-draw-with-list-view-controls"></a>Dibujo personalizado con List-View controles

Dado que los controles de vista de lista tienen subelementos y varios modos de presentación, deberá controlar la notificación [ \_ CUSTOMDRAW](nm-customdraw.md) de NM de forma ligeramente diferente que para los demás controles comunes.

Para el modo de informe, use el procedimiento siguiente.

1.  La primera [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) tendrá el miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada establecida en CDDS \_ PREPAINT. Devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  A continuación, recibirá una [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT. Si especifica nuevas fuentes o colores y devuelve [**CDRF \_ NEWFONT,**](cdrf-constants.md)se cambiarán todos los subelementos del elemento. Si en su lugar desea controlar cada subelemento por separado, devuelva [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md).
3.  Si devolvió [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) en el paso anterior, recibirá una notificación [NM \_ CUSTOMDRAW](nm-customdraw.md) para cada subelemento con **dwDrawStage** establecido en CDDS \_ SUBITEM \| CDDS \_ ITEMPREPAINT. Para cambiar la fuente o el color de ese subelemento, especifique una nueva fuente o color y devuelva [**\_ CDRF NEWFONT**](cdrf-constants.md).

Para el icono grande, el icono pequeño y los modos de lista, use el procedimiento siguiente.

1.  La primera [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) tendrá el miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada establecida en CDDS \_ PREPAINT. Devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  A continuación, recibirá una [notificación \_ NM CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT. Puede cambiar las fuentes o los colores de un elemento especificando nuevas fuentes y colores y devolviendo [**\_ CDRF NEWFONT**](cdrf-constants.md). Dado que estos modos no tienen subelementos, no recibirá ninguna notificación adicional de NM \_ CUSTOMDRAW.

Para obtener un ejemplo de un controlador de notificación [NM \_ CUSTOMDRAW](nm-customdraw.md) de vista de lista, vea [Using Custom Draw](using-custom-draw.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Usar dibujo personalizado](using-custom-draw.md)
</dt> <dt>

[Referencia de dibujo personalizado](custom-draw-reference.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[EJEMPLO: CustDTv ilustra el dibujo personalizado en un treeview (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 