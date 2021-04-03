---
title: Propiedades y métodos
description: Al igual que cualquier objeto OLE, un control proporciona gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075389"
---
# <a name="properties-and-methods"></a>Propiedades y métodos

Al igual que cualquier objeto OLE, un control proporciona gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.

Un control expone propiedades y métodos a través de la automatización OLE para que los contenedores puedan tener acceso a ellos bajo el control de un lenguaje de programación proporcionado por el contenedor.

Para admitir el acceso a las propiedades a través de una interfaz de usuario, un control proporciona páginas de propiedades, compatibilidad con \_ las propiedades de OLEIVERB, la exploración de propiedades y el enlace de datos mediante el cambio de propiedad notfications.

-   A través de las páginas de propiedades, un control puede mostrar sus propiedades, independientemente de su contenedor, si es necesario.
-   Al admitir \_ las propiedades de OLEIVERB, el elemento de propiedades se muestra en el menú del contenedor. A continuación, el usuario final puede seleccionar el elemento **propiedades** para ver las páginas de propiedades del control y modificar las propiedades.
-   La exploración por propiedad admite un contenedor que puede mostrar las propiedades del control como parte de una hoja de propiedades más grande que puede incluir propiedades de varios controles del contenedor.
-   A través de la notificación de cambio de propiedad, un control puede notificar a un cliente que sus propiedades tienen cambios, lo que permite al cliente realizar las acciones necesarias como resultado.

Para obtener más información, vea los temas siguientes:

-   [Propiedades del control](control-properties.md)
-   [Métodos de control](control-methods.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> <dt>

[Páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




