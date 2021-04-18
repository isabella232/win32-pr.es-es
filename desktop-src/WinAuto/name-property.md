---
title: Propiedad Name
description: La propiedad Name es una cadena utilizada por los clientes para identificar, buscar o anunciar un objeto para el usuario. Todos los objetos admiten la propiedad Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704664"
---
# <a name="name-property"></a>Propiedad Name

La propiedad **Name** es una cadena utilizada por los clientes para identificar, buscar o anunciar un objeto para el usuario. Todos los objetos admiten la propiedad **Name** .

Por ejemplo, el texto de un control de botón es su nombre, mientras que el nombre de un cuadro de lista o un control de edición es el texto estático que precede inmediatamente al control en el orden de tabulación. Incluso los objetos gráficos que no muestran un nombre proporcionan texto cuando se consulta la propiedad **Name** .

La propiedad **Name** se recupera llamando a [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).

## <a name="selecting-names"></a>Seleccionar nombres

El nombre de un objeto debe ser intuitivo para que los usuarios sepan el significado o el propósito del objeto. Además, la propiedad **Name** debe ser única relativa a cualquier objeto relacionado en el elemento primario.

La navegación dentro de las tablas presenta problemas especialmente difíciles para algunos usuarios. Por lo tanto, los desarrolladores de servidor deben hacer que los nombres de celda de tabla sean lo más descriptivos posible. Por ejemplo, puede crear un nombre de celda combinando los nombres de la fila y la columna que ocupa, como "a1". Sin embargo, suele ser mejor usar nombres más descriptivos, como "Nancy, febrero", donde "Nancy" es la fila actual y "febrero" es la columna actual.

## <a name="delegating-requests"></a>Delegación de solicitudes

Si un objeto no tiene acceso a su propiedad **Name** , delega las solicitudes a su elemento primario, identificando por su identificador secundario. Por ejemplo, si un cliente llama a la propiedad de **nombre** de un control de edición, el control de edición delega la consulta a su elemento primario, que devuelve el valor del control de texto estático que etiqueta el control de edición.

 

 




