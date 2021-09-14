---
title: Objetos incrustados (COM)
description: Objetos incrustados
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242889"
---
# <a name="embedded-objects-com"></a>Objetos incrustados (COM)

Un objeto incrustado se almacena físicamente en el documento compuesto, junto con toda la información necesaria para administrar el objeto. En otras palabras, el objeto incrustado es realmente una parte del documento compuesto en el que reside. Esta disposición tiene un par de desventajas. En primer lugar, un documento compuesto que contenga objetos incrustados será mayor que uno que contenga los mismos objetos que los vínculos. En segundo lugar, los cambios realizados en el origen de un objeto incrustado no se replicarán automáticamente en la copia insertada y los cambios en la copia insertada no se reflejarán en el origen, ya que están con un vínculo.

Aun así, para determinados propósitos, la inserción ofrece varias ventajas con respecto a los vínculos. En primer lugar, los usuarios pueden transferir documentos compuestos con objetos incrustados a otros equipos u otras ubicaciones del mismo equipo, sin romper un vínculo. En segundo lugar, los usuarios pueden editar objetos incrustados sin cambiar el contenido del original. A veces, esta separación es exactamente lo que se requiere. En tercer lugar, los objetos incrustados se pueden activar en su lugar, lo que significa que el usuario puede editar o manipular el objeto sin tener que trabajar en una ventana independiente de la del contenedor del objeto. En su lugar, cuando se activa el objeto, la interfaz de usuario de la aplicación contenedora cambia para exponer las herramientas necesarias para administrar o modificar el objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear objetos vinculados e incrustados a partir de datos existentes](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




