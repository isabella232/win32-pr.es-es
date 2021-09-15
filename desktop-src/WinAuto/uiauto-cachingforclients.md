---
title: Almacenar en Automatización de la interfaz de usuario propiedades y patrones de control
description: Al usar Microsoft Automatización de la interfaz de usuario, los clientes a menudo necesitan recuperar varias propiedades para varios elementos de automatización.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- caching,Automatización de la interfaz de usuario propiedades
- caching,properties
- caching,Automatización de la interfaz de usuario de control
- almacenamiento en caché, patrones de control
- Automatización de la interfaz de usuario, propiedades de almacenamiento en caché
- Automatización de la interfaz de usuario,property caching
- clients,caching Automatización de la interfaz de usuario properties
- clients,caching Automatización de la interfaz de usuario de control
- Automatización de la interfaz de usuario, patrones de control de almacenamiento en caché
- Automatización de la interfaz de usuario, almacenamiento en caché de patrones de control
- patrones de control, almacenamiento en caché
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f75a7dc9491565fdfdc0ecc73808c2fb6a9d82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567328"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Almacenar en Automatización de la interfaz de usuario propiedades y patrones de control

Al usar Microsoft Automatización de la interfaz de usuario, los clientes a menudo necesitan recuperar varias propiedades para varios elementos de automatización. Un cliente podría recuperar propiedades individuales de un elemento a la vez mediante los métodos de recuperación de propiedades [**como IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CurrentAccessKey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey). Sin embargo, este método es lento e ineficaz porque requiere una llamada entre procesos para cada propiedad que se va a recuperar. Para mejorar el rendimiento, los clientes pueden usar las funcionalidades de almacenamiento en caché (también denominada captura masiva) de Automatización de la interfaz de usuario. El almacenamiento en caché permite a un cliente recuperar todas las propiedades deseadas para todos los elementos deseados con una sola llamada a método. A continuación, el cliente puede recuperar las propiedades individuales de la memoria caché según sea necesario y puede obtener una nueva instantánea de la memoria caché periódicamente, generalmente en respuesta a eventos que significan cambios en la interfaz de usuario.

La aplicación puede solicitar el almacenamiento en caché cuando recupera un elemento Automatización de la interfaz de usuario mediante un método, como [**IUIAutomation::ElementFromPointBuildCache,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache) [**IUIAutomationTreeWalker::GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)o [**IUIAutomationElement::FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache).

El almacenamiento en caché también se produce cuando se especifica una solicitud de caché al suscribirse a eventos. El Automatización de la interfaz de usuario elemento pasado al controlador de eventos como origen de un evento contiene las propiedades almacenadas en caché y los patrones de control especificados por la solicitud de caché. Los cambios realizados en la solicitud de caché después de suscribirse al evento no tienen ningún efecto.

En este tema se incluyen las siguientes secciones.

-   [Solicitudes de caché](#cache-requests)
    -   [Especificar la propiedad y los patrones de control que se almacenarán en caché](#specifying-property-and-control-patterns-to-cache)
    -   [Especificar el ámbito y el filtrado de una solicitud de almacenamiento en caché](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Intensidad de las referencias de elementos](#strength-of-element-references)
-   [Recuperación de elementos primarios y secundarios almacenados en caché](#retrieving-cached-children-and-parents)
-   [Recuperar una nueva instantánea de la caché](#retrieving-a-new-snapshot-of-the-cache)
-   [Ejemplos](#examples)
-   [Temas relacionados](#related-topics)

## <a name="cache-requests"></a>Solicitudes de caché

El almacenamiento en caché implica determinar qué propiedades recuperar y de qué elementos recuperarlas y, a continuación, usar esta información para crear una solicitud de caché. Cada vez que el cliente obtiene una interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el elemento de interfaz de usuario, Automatización de la interfaz de usuario almacena en caché la información especificada en la solicitud de caché.

Para crear una solicitud de caché, empiece por usar el método [**IUIAutomation::CreateCacheRequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) para recuperar un puntero de interfaz [**IUIAutomationCacheRequest.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) A continuación, configure la solicitud de caché mediante los métodos de **IUIAutomationCacheRequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Especificar la propiedad y los patrones de control que se almacenarán en caché

Puede especificar propiedades para almacenar en caché llamando a [**IUIAutomationCacheRequest::AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty). Puede especificar patrones de control para almacenar en caché mediante una [**llamada a IUIAutomationCacheRequest::AddPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern). Cuando un patrón de control se almacena en caché, sus propiedades no se almacenan automáticamente en caché; debe especificar las propiedades que desea almacenar en caché mediante **AddProperty**.

Puede recuperar una propiedad de patrón de control (por ejemplo, la propiedad Value del patrón de control [Value),](uiauto-implementingvalue.md) sin tener que recuperar todo el patrón de control en la memoria caché. Solo debe recuperar el patrón de control si necesita usar un método de patrón de control.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Especificar el ámbito y el filtrado de una solicitud de almacenamiento en caché

Puede especificar los elementos cuyas propiedades y patrones de control desea almacenar en caché estableciendo la propiedad [**IUIAutomationCacheRequest::TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) antes de usar la solicitud. El ámbito es relativo a los elementos recuperados por el método al que se pasa la solicitud de caché. Por ejemplo, si establece solo [**TreeScope \_ Children**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)y, a continuación, recupera un elemento Automatización de la interfaz de usuario, las propiedades y los patrones de control de los elementos secundarios de ese elemento se almacenan en caché, pero las propiedades y los patrones de control del propio elemento no se almacenan en caché. Para asegurarse de que el almacenamiento en caché se realiza para el propio elemento recuperado, debe incluir el elemento **\_ TreeScope** en la **propiedad IUIAutomationCacheRequest::TreeScope.** No es posible establecer el ámbito en **TreeScope \_ Parent** o **TreeScope \_ Ancestors**. Sin embargo, es posible almacenar en caché un elemento primario cuando se almacena un elemento secundario en caché; consulte la sección Recuperación de elementos primarios y secundarios almacenados en caché de este tema.

La extensión del almacenamiento en caché también se ve afectada por la [**propiedad IUIAutomationCacheRequest::TreeFilter.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) De forma predeterminada, el almacenamiento en caché solo se realiza para los elementos que aparecen en la vista de control Automatización de la interfaz de usuario árbol. Sin embargo, puede cambiar esta propiedad para aplicar el almacenamiento en caché a todos los elementos o solo a los que aparecen en la vista de contenido.

### <a name="strength-of-element-references"></a>Intensidad de las referencias de elementos

Al recuperar un elemento de automatización, de forma predeterminada tiene acceso a todas las propiedades y patrones de control de ese elemento, incluidas las propiedades y los patrones de control que no se almacenaron en caché. Sin embargo, puede especificar que la referencia al elemento haga referencia solo a los datos almacenados en caché estableciendo la propiedad [**IUIAutomationCacheRequest::AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) en **AutomationElementMode \_ None**. En este caso, no tiene acceso a las propiedades no en caché ni a los patrones de control de los elementos recuperados. Esto significa que no se puede acceder a ninguna propiedad actual como [**IUIAutomationElement::CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) ni recuperar un patrón de control mediante [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern). En los patrones de control almacenados en caché, no se puede llamar a métodos que realizan acciones en el control, como [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Un ejemplo de una aplicación que podría no necesitar referencias completa a objetos es un lector de pantalla, que podría precarga las propiedades de nombre y tipo de control de los elementos de una ventana sin necesidad de los propios objetos de elemento de automatización.

## <a name="retrieving-cached-children-and-parents"></a>Recuperación de elementos primarios y secundarios almacenados en caché

Al recuperar un elemento de automatización y el almacenamiento en caché de solicitudes para los elementos secundarios de ese elemento a través de la propiedad [**IUIAutomationCacheRequest::TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) de la solicitud, es posible obtener los elementos secundarios mediante una llamada a [**IUIAutomationElement::GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) en el elemento recuperado.

Si [**el \_ elemento TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) se incluyó en el ámbito de la solicitud de caché, el elemento raíz de la solicitud se puede recuperar llamando a [**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) en cualquiera de los elementos secundarios.

> [!Note]  
> No se pueden almacenar en caché los elementos primarios o antecesores del elemento raíz de la solicitud.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Recuperar una nueva instantánea de la caché

La memoria caché solo es válida siempre que no cambie nada en la interfaz de usuario. La aplicación es responsable de recuperar una nueva instantánea de la memoria caché, normalmente, en respuesta a eventos.

Si se suscribe a un evento con una solicitud de caché, obtiene una nueva instantánea [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de la memoria caché como origen del evento cada vez que se llama al controlador de eventos. También puede recuperar una nueva instantánea de información almacenada en caché para un elemento llamando a [**IUIAutomationElement::BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache). Puede pasar la [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) original para obtener una nueva instantánea de toda la información almacenada previamente en caché.

La recuperación de una nueva instantánea de la memoria caché no modifica las propiedades de las referencias [**existentes de IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)

## <a name="examples"></a>Ejemplos

Para obtener ejemplos de código que muestran cómo usar las funcionalidades de almacenamiento en caché de Automatización de la interfaz de usuario, vea [Cómo usar el almacenamiento en caché.](uiauto-howto-use-caching.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> </dl>

 

 




