---
title: Enlace de datos a través de IPropertyNotifySink
description: Enlace de datos a través de IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d39c7277d27f0df6c185fc35a926aa98b77b91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779800"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Enlace de datos a través de IPropertyNotifySink

Los objetos que admiten propiedades, por ejemplo, a través de la automatización OLE y la interfaz **IDispatch** , pueden querer permitir a los clientes recibir una notificación cuando ciertas propiedades cambian de valor. Este tipo de propiedad se denomina propiedad enlazable porque las notificaciones permiten a un cliente sincronizar su propia presentación de los valores de propiedad actuales del objeto. Además, es posible que los mismos objetos deseen permitir que un cliente controle cuándo se permite cambiar determinadas propiedades. Tales propiedades se denominan propiedades de edición de solicitud.

[**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) es una interfaz de notificación estándar que admite propiedades enlazables y de solicitud-modificación. **IPropertyNotifySink** se admite desde un objeto con propiedades como una interfaz de salida. Es decir, la propia interfaz se implementa mediante el objeto de receptor del cliente y el cliente conecta el receptor al objeto auxiliar a través del mecanismo de punto de conexión descrito anteriormente. **IPropertyNotifySink** se define de la siguiente manera:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Cuando un objeto desea notificar a sus receptores conectados que se ha cambiado una propiedad enlazable identificada con un DISPID determinado, llama a en el [**cambio**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Si un objeto cambia varias propiedades a la vez, puede pasar DISPID \_ Unknown a **onchange** , en cuyo caso un cliente actualiza su caché de todos los valores de propiedad de interés.

Cuando una propiedad de edición de solicitud está a punto de cambiar, un objeto puede preguntar al cliente si permite que se produzca ese cambio. El objeto llama a [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) pasando el DISPID de la propiedad en cuestión (o DISPID \_ Unknown para identificar todas las propiedades). El receptor del cliente devuelve S \_ OK para indicar que el cambio se permite o s \_ false (o un error) para indicar que no se permite el cambio. Cuando un objeto llama a **OnRequestEdit**, es necesario obedecer los deseos del cliente mediante la semántica exacta de \_ \_ los valores devueltos de s OK y s false.

Tenga en cuenta que [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) no se puede usar para la validación de datos porque en el momento de la llamada, el nuevo valor de la propiedad todavía no está disponible. La notificación solo se puede usar para controlar un estado de solo lectura para una propiedad.

Los objetos controlan las propiedades que se pueden enlazar y la edición de solicitud y marcan estas propiedades en la información de tipo del objeto. En la información de tipo, el atributo enlazable marca una propiedad como compatible con el [**modificador**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). El atributo requestedit marca una propiedad como compatible con [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit).

Una propiedad puede admitir ambos comportamientos, en cuyo caso se llama primero a [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) , y solo si se permite cambiar, se llama a la propiedad [**onchange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) .

La única excepción al comportamiento de estas propiedades es que no se envía ninguna notificación como resultado de los procedimientos de inicialización o carga de un objeto. En ese momento, se supone que todas las propiedades cambian y que todas deben tener permiso para cambiar. Por lo tanto, las notificaciones a esta interfaz son solo significativas en el contexto de un objeto completamente inicializado o cargado.

Se pueden aplicar otros dos atributos a las propiedades de la información de tipo de un objeto. El atributo defaultbind marca una propiedad enlazable como la que mejor representa el estado del objeto en su totalidad. El atributo displaybind marca una propiedad enlazable como adecuada para su presentación en la propia interfaz de usuario de un cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




