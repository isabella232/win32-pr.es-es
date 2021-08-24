---
title: Elementos recientes
description: La lista Elementos recientes es un panel del menú Aplicación que muestra los elementos usados más recientemente (MRU) para una aplicación.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1d67c38e1eb9014cfd3349881ed2849755ebc89489cc925052aa690f54adc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810895"
---
# <a name="recent-items"></a>Elementos recientes

La lista Elementos recientes es un panel del menú [Aplicación](windowsribbon-controls-applicationmenu.md) que muestra los elementos usados más recientemente (MRU) para una aplicación.

-   [Detalles](#details)
-   [Propiedades de elementos recientes](#recent-items-properties)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la captura de pantalla siguiente se muestra una lista de elementos recientes de WordPad para Windows 7).

![captura de pantalla de la lista de elementos recientes en la cinta de microsoft paint.](images/controls/recentitems.png)

El [menú](windowsribbon-controls-applicationmenu.md) Aplicación puede tener como máximo una lista [**ApplicationMenu.RecentItems,**](windowsribbon-element-applicationmenu-recentitems.md) representada por un elemento **ApplicationMenu.RecentItems,** para mostrar documentos recientes, imágenes, películas y otros proyectos en los que un usuario ha estado trabajando. El número de elementos enumerados oscila entre cero y el número máximo especificado en el marcado, con un valor predeterminado de diez. Los elementos recientes se muestran como una lista numerada de cadenas que indican nombres de archivo. Se recomienda usar la propiedad [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) para proporcionar la ruta de acceso completa de la ubicación del archivo, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de una lista de elementos recientes en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitems.png)

El [**elemento RecentItems**](windowsribbon-element-recentitems.md) tiene un atributo *EnablePinning* que, si se establece en , muestra un icono de anclar a la derecha de cada elemento de la lista, como se muestra en la siguiente captura `true` de pantalla.

> [!Note]  
> La anclación está habilitada de forma predeterminada si no se especifica el atributo *EnablePinning.*

 

![captura de pantalla de los elementos recientes anclados en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitemspinned.png)

El algoritmo de anclado está pensado para evitar que los elementos se ale de la **lista Elementos recientes.** El algoritmo genera el comportamiento siguiente:

-   Siempre se agrega un nuevo elemento en la parte superior de la **lista Elementos** recientes.
-   Los elementos se moverán hacia abajo en la lista con el tiempo. Una vez que la lista está completa (alcanza el número máximo de elementos especificado en el marcado), los elementos más antiguos quedan fuera de la parte inferior de la lista a medida que se agregan nuevos elementos a la parte superior de la lista.
-   Si un elemento ya aparece en algún lugar de la lista pero se vuelve a acceder a él, vuelve a la parte superior de la lista.
-   Si un elemento está anclado, seguirá bajando por la lista, pero no se desactivará en la parte inferior. En su lugar, una vez que la lista esté completa, el primer elemento desanclarado encima del elemento anclado se desactivará cuando se agrega un nuevo elemento a la lista.
-   Si el número de elementos anclados alcanza alguna vez el número máximo de elementos, no se agregará ningún elemento nuevo a la lista hasta que se desanclar un elemento.

## <a name="recent-items-properties"></a>Propiedades de elementos recientes

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Elementos recientes.

Normalmente, una propiedad Elementos recientes se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El evento de invalidación se controla y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación ha consultado un valor de propiedad actualizado, hasta que el marco requiere la propiedad . Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Elementos recientes.



| Clave de propiedad                                                                       | Notas                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Información sobre \_ claves PKEY \_ de la interfaz de usuario](windowsribbon-reference-properties-uipkey-keytip.md)           | Solo se puede actualizar a través de la invalidación. |
| [Elementos \_ recientes de PKEY de la interfaz de \_ usuario](windowsribbon-reference-properties-uipkey-recentitems.md) | Solo se puede actualizar a través de la invalidación. |



 

## <a name="remarks"></a>Comentarios

El [método IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) se puede usar para recuperar la lista de MRU Windows Shell para la aplicación ribbon. A continuación, la aplicación puede usar el objeto recuperado por este método  para crear los datos requeridos por el marco de la cinta de opciones para rellenar la lista Elementos recientes del [menú Aplicación](windowsribbon-controls-applicationmenu.md).

> [!Note]  
> Cuando se usa este método, *listtype* debe tener el valor `ADLT_RECENT` .

 

Para obtener un ejemplo de cómo implementar una lista de elementos de MRU en una aplicación de marco de cinta de opciones, vea el ejemplo [HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado Elementos recientes**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 