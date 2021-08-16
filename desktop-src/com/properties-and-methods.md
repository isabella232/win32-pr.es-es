---
title: Propiedades y métodos
description: Al igual que cualquier objeto OLE, un control proporciona gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52dae30453089f235a4e70d7896569ebefcdff9f7f2419b5fc54af88b8563d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047893"
---
# <a name="properties-and-methods"></a>Propiedades y métodos

Al igual que cualquier objeto OLE, un control proporciona gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.

Un control expone propiedades y métodos a través de la automatización OLE para que los contenedores puedan acceder a ellas bajo el control de un lenguaje de programación proporcionado por contenedor.

Para admitir el acceso a las propiedades a través de una interfaz de usuario, un control proporciona páginas de propiedades, compatibilidad con PROPIEDADES OLEIVERB, exploración por propiedad y enlace de datos a través de \_ notficaciones de cambio de propiedad.

-   A través de páginas de propiedades, un control puede mostrar sus propiedades, independientemente de su contenedor, si es necesario.
-   Al admitir OLEIVERB \_ PROPERTIES, el elemento Propiedades se muestra en el menú del contenedor. A continuación, el usuario final puede seleccionar el **elemento Propiedades** para ver las páginas de propiedades del control y modificar las propiedades.
-   La exploración por propiedad admite un contenedor que puede mostrar las propiedades del control como parte de una hoja de propiedades más grande que puede incluir propiedades de varios controles del contenedor.
-   A través de la notificación de cambio de propiedad, un control puede notificar a un cliente que sus propiedades han cambiado, lo que permite al cliente realizar las acciones necesarias como resultado.

Para obtener más información, vea los temas siguientes:

-   [Propiedades del control](control-properties.md)
-   [Métodos de control](control-methods.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> <dt>

[Páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




