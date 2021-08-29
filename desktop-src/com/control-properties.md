---
title: Propiedades del control
description: Propiedades del control
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5dcc0dc0b546228c20b07a7a176d33972c306e6c1f38c6355ad99087551333
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048463"
---
# <a name="control-properties"></a>Propiedades del control

Además de las propiedades definidas e implementadas por el propio control, ActiveX tecnología de controles también implica:

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propiedades ambientales
</dt> <dd>

El contenedor los expone a través de un sitio cliente de control para proporcionar valores de entorno que se aplican a todos los controles insertados en el contenedor. Por ejemplo, un contenedor puede proporcionar un color de fondo predeterminado o una fuente predeterminada que el control puede usar. Las propiedades ambientales se exponen a través **de IDispatch** implementado en el objeto de sitio de un contenedor. El contenedor llama al método [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) del control cuando cualquiera de sus propiedades ambientales cambia el valor. En respuesta, es posible que un control deba actualizar su propio estado interno o visual en respuesta. El contenedor indica qué propiedad ambiental ha cambiado con el parámetro DISPID o puede pasar DISPID UNKNOWN para indicar que han cambiado \_ varias propiedades ambientales.

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propiedades extendidas
</dt> <dd>

Estos son realmente implementados por un contenedor para encapsular los controles que contiene para proporcionar propiedades administradas por contenedores que aparecen como si fueran propiedades de control nativas. El contenedor puede agregar el control, agregando las propiedades extendidas para complementar o invalidar las propiedades del control. El objeto agregado se denomina control extendido. En el contenedor, el control extendido aparece como el propio control y el control parece exponer las propiedades extendidas. El contenedor admite un control extendido a través de su método de sitio de cliente [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol). El **método GetExtendedControl** permite a los controles navegar por el sitio hasta el objeto de control extendido que les proporciona el contenedor, si el contenedor admite esta característica. Un contenedor también puede optar por mostrar páginas de propiedades para sus controles extendidos además de las páginas que un control normalmente especificaría a través de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Por este problema, un control tiene que pedir a un contenedor que muestre un marco de propiedades antes de que el control intente hacerlo por sí mismo. Para ello, el control llama a [**IOleControlSite::ShowPropertyFrame.**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) Si el contenedor implementa esta función, muestra el propio marco de propiedades; Si el método devuelve un error, el control puede mostrar el marco de propiedades.

</dd> </dl>

Para obtener más información, vea los temas siguientes:

-   [Propiedades estándar](standard-properties.md)
-   [Objeto de fuente estándar](standard-font-object.md)
-   [Objeto De imagen estándar](standard-picture-object.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de control](control-methods.md)
</dt> </dl>

 

 




