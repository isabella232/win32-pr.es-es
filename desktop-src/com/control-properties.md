---
title: Propiedades del control
description: Propiedades del control
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903852"
---
# <a name="control-properties"></a>Propiedades del control

Además de las propiedades definidas e implementadas por el propio control, la tecnología de controles ActiveX también implica:

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propiedades de ambiente
</dt> <dd>

Los expone el contenedor a través de un sitio de cliente de control para proporcionar valores de entorno que se aplican a todos los controles insertados en el contenedor. Por ejemplo, un contenedor puede proporcionar un color de fondo predeterminado o una fuente predeterminada que el control puede utilizar. Las propiedades de ambiente se exponen a través de **IDispatch** implementadas en el objeto de sitio de un contenedor. El contenedor llama al método [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) del control cuando alguna de sus propiedades de ambiente cambian de valor. En respuesta, es posible que un control tenga que actualizar su propio estado interno o visual en respuesta. El contenedor indica qué propiedad ambiente cambió con el parámetro DISPID o puede pasar DISPID \_ Unknown para indicar que han cambiado varias propiedades de ambiente.

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propiedades extendidas
</dt> <dd>

En realidad, los implementa un contenedor para encapsular los controles que contiene para proporcionar propiedades administradas por contenedores que aparecen como si fueran propiedades de control nativas. El contenedor puede Agregar el control agregando las propiedades extendidas para complementar o reemplazar las propiedades del control. El objeto agregado se denomina control extendido. En el contenedor, el control extendido aparece como el control en sí y las propiedades extendidas parecen expuestas por el control. El contenedor admite un control extendido a través de su método de sitio de cliente [**IOleControlSite:: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol). El método **GetExtendedControl** permite que los controles naveguen por el sitio hasta el objeto de control extendido proporcionado por el contenedor, si el contenedor es compatible con esta característica. Un contenedor también puede optar por mostrar las páginas de propiedades de sus controles extendidos además de las páginas que un control especificaría normalmente a través de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Por este motivo, un control tiene que pedir a un contenedor que muestre un marco de propiedades antes de que el control intente hacerlo. El control llama a [**IOleControlSite:: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) para hacerlo. Si el contenedor implementa esta función, muestra el propio marco de propiedades; Si el método devuelve un error, el control puede mostrar el marco de propiedad.

</dd> </dl>

Para obtener más información, vea los temas siguientes:

-   [Propiedades estándar](standard-properties.md)
-   [Objeto de fuente estándar](standard-font-object.md)
-   [Objeto de imagen estándar](standard-picture-object.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de control](control-methods.md)
</dt> </dl>

 

 




