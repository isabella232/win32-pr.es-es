---
title: Propiedad Name
description: La propiedad Name es una cadena que usan los clientes para identificar, buscar o anunciar un objeto para el usuario. Todos los objetos admiten la propiedad Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce046ef693e9e52323cdb7484bbdc291127b958d88857de6a8be4522b88e33de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133778"
---
# <a name="name-property"></a>Propiedad Name

La **propiedad Name** es una cadena que usan los clientes para identificar, buscar o anunciar un objeto para el usuario. Todos los objetos admiten la **propiedad Name.**

Por ejemplo, el texto de un control de botón es su nombre, mientras que el nombre de un cuadro de lista o control de edición es el texto estático que precede inmediatamente al control en el orden de tabulación. Incluso los objetos gráficos que no muestran un nombre proporcionan texto cuando se consulta para la **propiedad** Name.

La **propiedad Name** se recupera mediante una llamada a [**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).

## <a name="selecting-names"></a>Selección de nombres

El nombre de un objeto debe ser intuitivo para que los usuarios comprendan el significado o el propósito del objeto. Además, la **propiedad Name** debe ser única en relación con cualquier objeto relacionado del elemento primario.

La navegación dentro de tablas presenta problemas especialmente difíciles para algunos usuarios. Por lo tanto, los desarrolladores de servidores deben hacer que los nombres de celda de tabla sea lo más descriptivo posible. Por ejemplo, podría crear un nombre de celda combinando los nombres de la fila y columna que ocupa, como "A1". Sin embargo, por lo general es mejor usar nombres más descriptivos, como "Nancy, febrero", donde "Nancy" es la fila actual y "Febrero" es la columna actual.

## <a name="delegating-requests"></a>Delegación de solicitudes

Si un objeto no tiene acceso a su **propiedad Name,** delega las solicitudes a su elemento primario, identificándose por su identificador secundario. Por ejemplo, si un cliente llama a la propiedad Name de un control **de** edición, el control de edición delega la consulta en su elemento primario, que devuelve el valor del control de texto estático que etiqueta el control de edición.

 

 




