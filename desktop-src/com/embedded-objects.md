---
title: Objetos incrustados (COM)
description: Objetos incrustados
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df671850dc167a0751f69cbc57f8c19698db06a0454dd6283553c4d8ffa1609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048363"
---
# <a name="embedded-objects-com"></a>Objetos incrustados (COM)

Un objeto incrustado se almacena físicamente en el documento compuesto, junto con toda la información necesaria para administrar el objeto. En otras palabras, el objeto incrustado es realmente una parte del documento compuesto en el que reside. Esta disposición tiene un par de desventajas. En primer lugar, un documento compuesto que contenga objetos incrustados será mayor que uno que contenga los mismos objetos que los vínculos. En segundo lugar, los cambios realizados en el origen de un objeto incrustado no se replicarán automáticamente en la copia incrustada y los cambios en la copia incrustada no se reflejarán en el origen, ya que están con un vínculo.

Aun así, para determinados propósitos, la inserción ofrece varias ventajas con respecto a los vínculos. En primer lugar, los usuarios pueden transferir documentos compuestos con objetos incrustados a otros equipos u otras ubicaciones del mismo equipo, sin que se rompa un vínculo. En segundo lugar, los usuarios pueden editar objetos incrustados sin cambiar el contenido del original. A veces, esta separación es precisamente lo que se requiere. En tercer lugar, los objetos incrustados se pueden activar en su lugar, lo que significa que el usuario puede editar o manipular el objeto sin tener que trabajar en una ventana independiente de la del contenedor del objeto. En su lugar, cuando se activa el objeto , la interfaz de usuario de la aplicación contenedora cambia para exponer las herramientas necesarias para administrar o modificar el objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear objetos vinculados e incrustados a partir de datos existentes](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




