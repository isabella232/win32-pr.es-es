---
title: Elementos recientes
description: La lista Elementos recientes es un panel del menú Aplicación que muestra los elementos usados más recientemente (MRU) para una aplicación.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251727"
---
# <a name="recent-items"></a>Elementos recientes

La lista Elementos recientes es un panel del menú [Aplicación](windowsribbon-controls-applicationmenu.md) que muestra los elementos usados más recientemente (MRU) para una aplicación.

-   [Detalles](#details)
-   [Propiedades de elementos recientes](#recent-items-properties)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la siguiente captura de pantalla se muestra una lista de elementos recientes de WordPad para Windows 7).

![captura de pantalla de la lista de elementos recientes en la cinta de microsoft paint.](images/controls/recentitems.png)

El [menú de](windowsribbon-controls-applicationmenu.md) la aplicación puede tener como máximo una lista [**ApplicationMenu.RecentItems,**](windowsribbon-element-applicationmenu-recentitems.md) representada por un elemento **ApplicationMenu.RecentItems,** para mostrar documentos recientes, imágenes, películas y otros proyectos en los que un usuario ha estado trabajando. El número de elementos enumerados oscila entre cero y el número máximo especificado en el marcado, con un valor predeterminado de diez. Los elementos recientes se muestran como una lista numerada de cadenas que indican nombres de archivo. Se recomienda usar la [**propiedad Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) para proporcionar la ruta de acceso completa de la ubicación del archivo, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de una lista de elementos recientes en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitems.png)

El [**elemento RecentItems**](windowsribbon-element-recentitems.md) tiene un atributo *EnablePinning* que, si se establece en , muestra un icono de anclar a la derecha de cada elemento de la lista, como se muestra en la siguiente captura `true` de pantalla.

> [!Note]  
> La anclación está habilitada de forma predeterminada si no se especifica el atributo *EnablePinning.*

 

![captura de pantalla de elementos recientes anclados en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitemspinned.png)

El algoritmo de anclado está pensado para evitar que los elementos se alegar de la **lista Elementos recientes.** El algoritmo genera el comportamiento siguiente:

-   Siempre se agrega un nuevo elemento en la parte superior de la **lista Elementos** recientes.
-   Los elementos se moverán hacia abajo en la lista con el tiempo. Una vez que la lista está completa (alcanza el número máximo de elementos especificado en el marcado), los elementos más antiguos se quedan fuera de la parte inferior de la lista a medida que se agregan nuevos elementos a la parte superior de la lista.
-   Si un elemento ya aparece en algún lugar de la lista pero se vuelve a acceder a él, vuelve a la parte superior de la lista.
-   Si un elemento está anclado, seguirá recorriéndo la lista, pero no se desactivará en la parte inferior. En su lugar, una vez que la lista esté llena, el primer elemento desanclarado encima del elemento anclado se desactivará cuando se agrega un nuevo elemento a la lista.
-   Si el número de elementos anclados alcanza alguna vez el número máximo de elementos, no se agregará ningún elemento nuevo a la lista hasta que se desanclar un elemento.

## <a name="recent-items-properties"></a>Propiedades de elementos recientes

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control Elementos recientes.

Normalmente, una propiedad Elementos recientes se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Elementos recientes.



| Clave de propiedad                                                                       | Notas                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Información sobre \_ claves PKEY \_ de la interfaz de usuario](windowsribbon-reference-properties-uipkey-keytip.md)           | Solo se puede actualizar a través de la invalidación. |
| [Elementos \_ recientes de PKEY de la interfaz de \_ usuario](windowsribbon-reference-properties-uipkey-recentitems.md) | Solo se puede actualizar a través de la invalidación. |



 

## <a name="remarks"></a>Observaciones

El [método IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) se puede usar para recuperar la lista de MRU Windows Shell para la aplicación ribbon. A continuación, la aplicación puede usar el objeto recuperado por este método  para crear los datos requeridos por el marco de la cinta de opciones para rellenar la lista Elementos recientes del [menú de la aplicación](windowsribbon-controls-applicationmenu.md).

> [!Note]  
> Al usar este método, *listtype* debe tener el valor `ADLT_RECENT` .

 

Para obtener un ejemplo de cómo implementar una lista de elementos de MRU en una aplicación de marco de cinta de opciones, vea el [ejemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado De elementos recientes**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 