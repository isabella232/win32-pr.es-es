---
title: Enlace de datos a través de IPropertyNotifySink
description: Enlace de datos a través de IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337233455872928f824d8cbb903aba247b1ef496d02c0af04223361731fe3663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854655"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Enlace de datos a través de IPropertyNotifySink

Los objetos que admiten propiedades, por ejemplo, a través de OLE Automation y la interfaz **IDispatch,** pueden querer permitir que se notifique a los clientes cuando determinadas propiedades cambien el valor. Esta propiedad se denomina propiedad enlazable porque las notificaciones permiten a un cliente sincronizar su propia presentación de los valores de propiedad actuales del objeto. Además, es posible que los mismos objetos deseen permitir que un cliente controle cuándo pueden cambiar ciertas propiedades. Estas propiedades se denominan propiedades de edición de solicitudes.

[**IPropertyNotifySink es**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) una interfaz de notificación estándar que admite propiedades enlazables y de edición de solicitudes. **IPropertyNotifySink** se admite desde un objeto con propiedades como interfaz saliente. Es decir, la propia interfaz se implementa mediante el objeto receptor de un cliente y el cliente conecta el receptor al objeto de soporte a través del mecanismo de punto de conexión descrito anteriormente. **IPropertyNotifySink** se define de la siguiente manera:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Cuando un objeto desea notificar a sus receptores conectados que ha cambiado una propiedad enlazable identificada con un DISPID determinado, llama a [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Si un objeto cambia varias propiedades a la vez, puede pasar DISPID \_ UNKNOWN a **OnChanged,** en cuyo caso un cliente actualiza su memoria caché de todos los valores de propiedad de interés.

Cuando una propiedad de edición de solicitud está a punto de cambiar, un objeto puede preguntar al cliente si permitirá que se produzca ese cambio. El objeto llama a [**OnRequestEdit pasando**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) el DISPID de la propiedad en cuestión (o DISPID \_ UNKNOWN para identificar todas las propiedades). El receptor del cliente devuelve S OK para indicar que se permite el cambio, o S FALSE (o un error) para indicar que no \_ \_ se permite el cambio. Cuando un objeto llama a **OnRequestEdit**, es necesario cumplir los deseo del cliente siguiendo la semántica exacta de los valores devueltos S OK y \_ S \_ FALSE.

Tenga en [**cuenta que OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) no se puede usar para la validación de datos porque, en el momento de la llamada, el nuevo valor de la propiedad aún no está disponible. La notificación solo se puede usar para controlar un estado de solo lectura para una propiedad.

Los objetos controlan qué propiedades son enlazables y solicitan editar y marcar dichas propiedades en la información de tipo del objeto. En la información de tipo, el atributo enlazable marca una propiedad como compatible con [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). El atributo requestedit marca una propiedad como compatible con [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit).

Una propiedad puede admitir ambos comportamientos, en cuyo caso se llama primero a [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) y solo si se permite el cambio se llama [**a OnChanged.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged)

La única excepción al comportamiento de estas propiedades es que no se envía ninguna notificación como resultado de los procedimientos de inicialización o carga de un objeto. En esos momentos, se supone que todas las propiedades cambian y que se debe permitir que todas cambien. Por lo tanto, las notificaciones a esta interfaz solo son significativas en el contexto de un objeto totalmente inicializado o cargado.

Se pueden aplicar otros dos atributos a las propiedades de la información de tipo de un objeto. El atributo defaultbind marca una propiedad enlazable como la que mejor representa el estado del objeto en su conjunto. El atributo displaybind marca una propiedad enlazable como adecuada para mostrarse en la propia interfaz de usuario de un cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




