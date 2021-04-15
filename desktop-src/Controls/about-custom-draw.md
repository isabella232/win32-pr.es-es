---
title: Acerca de Draw personalizado
description: Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información conceptual sobre cómo una aplicación puede admitir el dibujo personalizado.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121a4df5aa6fab222a5c4387ebdcfba51a7977b2
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104488441"
---
# <a name="about-custom-draw"></a>Acerca de Draw personalizado

Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información conceptual sobre cómo una aplicación puede admitir el dibujo personalizado. Actualmente, los controles siguientes admiten la funcionalidad de dibujo personalizada:

-   Controles de encabezado
-   Controles de vista de lista
-   Rebar (controles)
-   Controles de la barra de herramientas
-   Controles ToolTip
-   Controles TrackBar
-   Controles de vista de árbol

<!-- -->

-   [Acerca de los mensajes de notificación de dibujo personalizados](#about-custom-draw-notification-messages)
-   [Dibujar ciclos, fases de dibujo y mensajes de notificación](#paint-cycles-drawing-stages-and-notification-messages)
-   [Sacar provecho de los servicios de dibujo personalizados](#taking-advantage-of-custom-draw-services)
    -   [Respuesta a la notificación del problema](#responding-to-the-prepaint-notification)
    -   [Solicitud de notificaciones específicas del elemento](#requesting-item-specific-notifications)
    -   [Dibujo del elemento](#drawing-the-item-yourself)
    -   [Cambiar fuentes y colores](#changing-fonts-and-colors)
-   [Dibujo personalizado con controles de List-View y Tree-View](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Dibujo personalizado con controles de List-View](#custom-draw-with-list-view-controls)
-   [Temas relacionados](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Acerca de los mensajes de notificación de dibujo personalizados

Todos los controles comunes que admiten Draw personalizado envían códigos de notificación [ \_ CUSTOMDRAW nm](nm-customdraw.md) en puntos específicos durante las operaciones de dibujo. Estos códigos de notificación describen las operaciones de dibujo que se aplican a todo el control y a las operaciones de dibujo específicas de los elementos del control. Al igual que muchos códigos de notificación, las \_ notificaciones de nm CUSTOMDRAW se envían como mensajes de [**\_ notificación de WM**](wm-notify.md) .

El parámetro *lParam* de una notificación de dibujo personalizada será la dirección de una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) o una estructura específica del control que contenga una estructura **NMCUSTOMDRAW** como primer miembro. En la tabla siguiente se muestra la relación entre los controles y las estructuras que usan.



| Estructura                                | Usado por                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Rebar, TrackBar y controles de encabezado |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Controles de vista de lista                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Controles de la barra de herramientas                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Controles ToolTip                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Controles de vista de árbol                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Dibujar ciclos, fases de dibujo y mensajes de notificación

Al igual que todas las aplicaciones de Windows, los controles comunes se dibujan y borran de forma periódica en función de los mensajes recibidos del sistema o de otras aplicaciones. El proceso de dibujar o borrar un control se denomina *ciclo de pintura*. Los controles que admiten los códigos de notificación de envío de dibujo [nm \_ CUSTOMDRAW](nm-customdraw.md) personalizados periódicamente a través de cada ciclo de pintura. Este código de notificación está acompañado por una estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) u otra estructura que contiene una estructura **NMCUSTOMDRAW** como su primer miembro.

Una parte de la información que contiene la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es la fase actual del ciclo de pintura. Esto se conoce como la *fase de dibujo* y se representa mediante el valor del miembro **dwDrawStage** de la estructura. Un control informa A su elemento primario sobre cuatro fases básicas de Draw. Estas fases de dibujo básicas o globales se representan en la estructura mediante los siguientes valores de marca (definidos en commctrl. h).



| Valores de la fase de dibujo global | Descripción                        |
|--------------------------|------------------------------------|
| CDDS \_           | Antes de que comience el ciclo de pintura.     |
| CDDS \_ POSTpaint          | Una vez completado el ciclo de pintura. |
| CDDS \_ PREborrar           | Antes de que comience el ciclo de borrado.     |
| CDDS \_ POSTborrar          | Una vez completado el ciclo de borrado. |



 

Cada uno de los valores anteriores se puede combinar con la \_ marca del elemento CDDS para especificar las fases de dibujo específicas de los elementos. Por comodidad, commctrl. h contiene los siguientes valores específicos del elemento.



| Valores de fase de dibujo específicos del elemento | Descripción                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDDS \_ ITEMPREPAINT              | Antes de que se dibuje un elemento.                                                                                                                                                                                                                                                            |
| CDDS \_ ITEMPOSTPAINT             | Después de dibujar un elemento.                                                                                                                                                                                                                                                       |
| CDDS \_ ITEMPREERASE              | Antes de que se borre un elemento.                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | Una vez borrado un elemento.                                                                                                                                                                                                                                                      |
| subelemento CDDS \_                   | [Versiones de control comunes](common-control-versions.md) 4,71. Marca combinada con CDDS \_ ITEMPREPAINT o CDDS \_ ITEMPOSTPAINT si se está dibujando un subelemento. Solo se establecerá si [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) se devuelve desde CDDS \_ PREPAINT. |



 

La aplicación debe procesar el código de notificación [nm \_ CUSTOMDRAW](nm-customdraw.md) y, a continuación, devolver un valor específico que informa al control de lo que debe hacer. Vea las secciones siguientes para obtener más información sobre estos valores devueltos.

## <a name="taking-advantage-of-custom-draw-services"></a>Sacar provecho de los servicios de dibujo personalizados

La clave para aprovechar la funcionalidad de dibujo personalizada es responder a los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) que envía un control. Los valores devueltos que envía la aplicación en respuesta a estas notificaciones determinan el comportamiento del control para ese ciclo de pintura.

Esta sección contiene información sobre cómo la aplicación puede usar los valores de devolución de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) para determinar el comportamiento del control.

Los detalles se dividen en los temas siguientes:

-   [Respuesta a la notificación del problema](#responding-to-the-prepaint-notification)
-   [Solicitud de notificaciones específicas del elemento](#requesting-item-specific-notifications)
-   [Dibujo del elemento](#drawing-the-item-yourself)
-   [Cambiar fuentes y colores](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Respuesta a la notificación del problema

Al principio de cada ciclo de pintura, el control envía el código de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) , especificando el \_ valor de CDDS en el miembro **DWDRAWSTAGE** de la estructura de nm CUSTOMDRAW que lo acompaña \_ . El valor que devuelve la aplicación a esta primera notificación determina cómo y cuándo envía el control notificaciones de dibujo personalizadas posteriores para el resto del ciclo de pintura. La aplicación puede devolver una combinación de las marcas siguientes en respuesta a la primera notificación.



| Valor devuelto            | Efecto                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDRF \_ predeterminado         | El control se dibujará por sí mismo. No enviará más notificaciones de [nm \_ CUSTOMDRAW](nm-customdraw.md) para este ciclo de pintura. Esta marca no se puede usar con ningún otro marcador.                                                                                                                                                                                                                                                                               |
| CDRF \_           | El control solo dibujará el fondo.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, consulte [cambiar fuentes y colores](#changing-fonts-and-colors). Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | El control notificará al elemento primario de cualquier operación de dibujo específica del elemento. Enviará los códigos de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) antes y después de que dibuje los elementos. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | El control enviará una notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) cuando se complete el ciclo de dibujo para todo el control. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ PREPAINT.                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [Versión 4,71](common-control-versions.md). La aplicación recibirá una notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecida en CDDS \_ ITEMPREPAINT \| CDDS \_ SubItem antes de que se dibuje cada subelemento de vista de lista. Después, puede especificar la fuente y el color de cada subelemento por separado o devolver [**CDRF de \_ forma predeterminada**](cdrf-constants.md) para el procesamiento predeterminado. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT. |
| CDRF \_ SKIPDEFAULT       | La aplicación dibujó el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | El control no dibujará el rectángulo de foco alrededor de un elemento.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Solicitud de notificaciones específicas del elemento

Si la aplicación devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) a la notificación de dibujo personalizado del prepintado inicial, el control enviará notificaciones para cada elemento que dibuje durante dicho ciclo. Estas notificaciones específicas del elemento tendrán el valor CDDS \_ ITEMPREPAINT en el miembro **dwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) adjunta. Puede solicitar que el control envíe otra notificación cuando termine de dibujar el elemento devolviendo [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) a estas notificaciones específicas del elemento. De lo contrario, se devuelve [**CDRF de \_ forma predeterminada**](cdrf-constants.md) y el control no notificará a la ventana primaria hasta que empiece a dibujar el elemento siguiente.

### <a name="drawing-the-item-yourself"></a>Dibujo del elemento

Si la aplicación dibuja todo el elemento, se devuelve [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md). Esto permite al control omitir los elementos que no necesita dibujar, con lo que se reduce la sobrecarga del sistema. Tenga en cuenta que devolver este valor significa que el control no dibujará ninguna parte del elemento.

### <a name="changing-fonts-and-colors"></a>Cambiar fuentes y colores

La aplicación puede usar Draw personalizado para cambiar la fuente de un elemento. Simplemente seleccione el HFONT que desee en el contexto de dispositivo especificado por el miembro **HDC** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada a la notificación de dibujo personalizada. Dado que la fuente que seleccione puede tener distintas métricas que la fuente predeterminada, asegúrese de incluir el bit [**CDRF \_ NEWFONT**](cdrf-constants.md) en el valor devuelto del mensaje de notificación. Para obtener más información sobre el uso de esta funcionalidad, consulte el código de ejemplo en [uso de Draw personalizado](using-custom-draw.md). La fuente que especifica la aplicación se usa para mostrar ese elemento cuando no está seleccionado. El dibujo personalizado no permite cambiar los atributos de fuente de los elementos seleccionados.

Para cambiar los colores de texto de todos los controles que admiten el dibujo personalizado excepto la vista de lista y la vista de árbol, simplemente establezca los colores de fondo y texto que desee en el contexto de dispositivo proporcionado en la estructura de notificación de dibujo personalizada con las funciones [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) y [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) . Para modificar los colores de texto en la vista de lista o en la vista de árbol, debe colocar los valores de color deseados en los miembros **clrText** y **clrTextBk** de la estructura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) o [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) .

> [!Note]  
> Antes de la [versión 6,0](common-control-versions.md) de los controles comunes, las barras de herramientas omiten la marca [**\_ NEWFONT de CDRF**](cdrf-constants.md) . La versión 6,0 admite la marca **\_ NEWFONT de CDRF** y se puede usar para seleccionar una fuente diferente para la barra de herramientas. Sin embargo, no se puede cambiar el color de una barra de herramientas cuando está activo un estilo visual. Para cambiar el color de una barra de herramientas en la versión 6,0, primero debe deshabilitar los estilos visuales mediante una llamada a [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) y no especificar ningún estilo visual:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Dibujo personalizado con controles de List-View y Tree-View

La mayoría de los controles comunes se pueden controlar en esencia de la misma manera. Sin embargo, los controles de vista de lista y de vista de árbol tienen algunas características que requieren un enfoque algo diferente para el dibujo personalizado.

En la [versión 5,0](common-control-versions.md), estos dos controles pueden mostrar texto recortado si cambia la fuente devolviendo [**CDRF \_ NEWFONT**](cdrf-constants.md). Este comportamiento es necesario para la compatibilidad con versiones anteriores de los controles comunes. Si desea cambiar la fuente de un control de vista de lista o de árbol, obtendrá mejores resultados si envía un mensaje [**\_ SETVERSION de CCM**](ccm-setversion.md) con el valor de *wParam* establecido en 5 antes de agregar elementos al control. Para obtener un ejemplo de un control de vista de árbol que usa Draw personalizado, vea el artículo de Knowledge base sobre el [ejemplo: CustDTv ilustra el uso de Draw personalizado en un TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496).

### <a name="custom-draw-with-list-view-controls"></a>Dibujo personalizado con controles de List-View

Dado que los controles de vista de lista tienen subelementos y varios modos de presentación, deberá controlar la notificación de [ \_ CUSTOMDRAW nm](nm-customdraw.md) de forma ligeramente diferente a la de los demás controles comunes.

En el modo de informe, utilice el procedimiento siguiente.

1.  La primera [notificación \_ CUSTOMDRAW de nm](nm-customdraw.md) tendrá el miembro **DwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada establecida en CDDS \_ PREPAINT. Devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Después recibirá una notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT. Si especifica nuevas fuentes o colores y devuelve [**CDRF \_ NEWFONT**](cdrf-constants.md), se cambiarán todos los subelementos del elemento. Si en su lugar desea controlar cada subelemento por separado, devuelva [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md).
3.  Si ha devuelto [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) en el paso anterior, recibirá una notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) para cada SUBelemento con **dwDrawStage** establecido en CDDS \_ SubItem \| CDDS \_ ITEMPREPAINT. Para cambiar la fuente o el color de ese subelemento, especifique una nueva fuente o color y devuelva [**CDRF \_ NEWFONT**](cdrf-constants.md).

En el caso de los modos de iconos grandes, iconos pequeños y listas, use el procedimiento siguiente.

1.  La primera [notificación \_ CUSTOMDRAW de nm](nm-customdraw.md) tendrá el miembro **DwDrawStage** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) asociada establecida en CDDS \_ PREPAINT. Devuelve [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Después recibirá una notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT. Puede cambiar las fuentes o los colores de un elemento especificando nuevas fuentes y colores y devolviendo [**CDRF \_ NEWFONT**](cdrf-constants.md). Dado que estos modos no tienen subelementos, no recibirá ninguna notificación adicional de NM \_ CUSTOMDRAW.

Para obtener un ejemplo de un controlador de notificación de la vista de lista [ \_ CUSTOMDRAW nm](nm-customdraw.md) , vea [usar Draw personalizado](using-custom-draw.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Usar Draw personalizado](using-custom-draw.md)
</dt> <dt>

[Referencia de dibujo personalizada](custom-draw-reference.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[EJEMPLO: CustDTv ilustra el dibujo personalizado en una vista de árbol (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 