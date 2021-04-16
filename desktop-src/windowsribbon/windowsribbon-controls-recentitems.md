---
title: Elementos recientes
description: La lista elementos recientes es un panel del menú aplicación que muestra los elementos usados más recientemente (MRU) para una aplicación.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566597"
---
# <a name="recent-items"></a>Elementos recientes

La lista elementos recientes es un panel del [menú aplicación](windowsribbon-controls-applicationmenu.md) que muestra los elementos usados más recientemente (MRU) para una aplicación.

-   [Detalles](#details)
-   [Propiedades de elementos recientes](#recent-items-properties)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la siguiente captura de pantalla se muestra una lista de elementos recientes de WordPad para Windows 7).

![captura de pantalla de la lista elementos recientes en la cinta de opciones de Microsoft Paint.](images/controls/recentitems.png)

El [menú aplicación](windowsribbon-controls-applicationmenu.md) puede tener como máximo una lista [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , representada por un elemento **ApplicationMenu. RecentItems** , para mostrar documentos recientes, imágenes, películas y otros proyectos en los que el usuario ha estado trabajando. El número de elementos de la lista va de cero al número máximo especificado en el marcado, con un valor predeterminado de diez. Los elementos recientes se muestran como una lista numerada de cadenas que indican los nombres de archivo. Se recomienda usar la propiedad [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) para proporcionar la ruta de acceso completa de la ubicación del archivo, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de una lista de elementos recientes en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitems.png)

El elemento [**RecentItems**](windowsribbon-element-recentitems.md) tiene un atributo *EnablePinning* que, si se establece en `true` , muestra un icono de anclaje a la derecha de cada elemento de la lista, como se muestra en la siguiente captura de pantalla.

> [!Note]  
> El anclaje está habilitado de forma predeterminada si no se especifica el atributo *EnablePinning* .

 

![captura de pantalla del anclaje de elementos recientes en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitemspinned.png)

El algoritmo de anclaje está diseñado para evitar que los elementos caigan en la lista de **elementos recientes** . El algoritmo produce el comportamiento siguiente:

-   Un nuevo elemento siempre se agrega en la parte superior de la lista de **elementos recientes** .
-   Los elementos se desactivarán en la lista a lo largo del tiempo. Una vez que la lista está llena (alcanza el número máximo de elementos especificado en el marcado), los elementos más antiguos quedan fuera de la parte inferior de la lista a medida que se agregan nuevos elementos a la parte superior de la lista.
-   Si un elemento ya aparece en alguna parte de la lista, pero se vuelve a acceder a él, se vuelve a colocar en la parte superior de la lista.
-   Si un elemento está anclado, seguirá desplazando la lista, pero no se cerrará la parte inferior. En su lugar, una vez completada la lista, el primer elemento desanclado situado encima del elemento anclado se desactivará cuando se agregue un nuevo elemento a la lista.
-   Si el número de elementos anclados alcanza siempre el número máximo de elementos, no se agregarán nuevos elementos a la lista hasta que se desancla un elemento.

## <a name="recent-items-properties"></a>Propiedades de elementos recientes

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de elementos recientes.

Normalmente, una propiedad de elementos recientes se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedades que están asociadas con el control de elementos recientes.



| Clave de propiedad                                                                       | Notas                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [KeyTip de UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-keytip.md)           | Solo se puede actualizar a través de la invalidación. |
| [UI \_ PKEY \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md) | Solo se puede actualizar a través de la invalidación. |



 

## <a name="remarks"></a>Observaciones

El método [IApplicationDocumentLists:: getList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) se puede usar para recuperar la lista MRU de Shell de Windows para la aplicación de cinta. A continuación, la aplicación puede usar el objeto recuperado por este método para crear los datos que requiere el marco de cinta para rellenar la lista de **elementos recientes** del menú de la [aplicación](windowsribbon-controls-applicationmenu.md).

> [!Note]  
> Cuando se usa este método, *ListType* debe tener el valor `ADLT_RECENT` .

 

Para obtener un ejemplo de cómo implementar una lista de elementos MRU en una aplicación de marco de cinta, vea el [ejemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado de elementos recientes**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 