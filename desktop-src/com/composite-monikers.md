---
title: Monikers compuestos
description: Una de las características más útiles de los monikers es que puede concatenar o componer monikers juntos.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5375bb505ff3737fb4e0cdea894790d93c0051
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369500"
---
# <a name="composite-monikers"></a>Monikers compuestos

Una de las características más útiles de los monikers es que puede concatenar o componer monikers juntos. Un *moniker compuesto es* un moniker que es una composición de otros monikers y puede determinar la relación entre las partes. Esto le permite ensamblar la ruta de acceso completa a un objeto dados dos o más monikers que son el equivalente de las rutas de acceso parciales. Puede crear monikers de la misma clase (por ejemplo, dos monikers de archivo) o de clases diferentes (como un moniker de archivo y un moniker de elemento). Si fuera a escribir su propia clase de moniker, también podría crear monikers con monikers de archivo o elemento. La ventaja básica de un compuesto es que proporciona un fragmento de código para implementar cada moniker posible que es una combinación de monikers más sencillos. Esto reduce significativamente la necesidad de clases de moniker personalizadas específicas.

Dado que los monikers de diferentes clases se pueden componer entre sí, los monikers proporcionan la capacidad de unir varios espacios de nombres. El sistema de archivos define un espacio de nombres común para los objetos almacenados como archivos porque todas las aplicaciones comprenden un nombre de ruta de acceso del sistema de archivos. De forma similar, un objeto contenedor también define un espacio de nombres privado para los objetos que contiene porque ningún contenedor entiende los nombres generados por otro contenedor. Los monikers permiten que estos espacios de nombres se unan porque se pueden crear monikers de archivos y monikers de elementos. Un cliente de moniker puede buscar en el espacio de nombres todos los objetos mediante un único mecanismo. El cliente simplemente llama [**a IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en el moniker y el código de moniker controla el resto. Una llamada a [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) en una composición crea un nombre mediante la concatenación de todos los nombres para mostrar de los monikers individuales.

Además, dado que puede escribir su propia clase de moniker, la composición de moniker le permite agregar extensiones personalizadas al espacio de nombres para los objetos .

A veces se pueden combinar dos monikers de clases específicas de una manera especial. Por ejemplo, un moniker de archivo que representa una ruta de acceso incompleta y otro moniker de archivo que representa una ruta de acceso relativa se pueden combinar para formar un moniker de archivo único que represente la ruta de acceso completa. Por ejemplo, los monikers de archivo "c: work art" se podrían componer con el \\ \\ moniker de archivo relativo ".. \\ backup \\myfile.doc" para que sea igual a "c: \\ work backup \\ \\myfile.doc". Este es un ejemplo de *composición no general.*

*Por otro* lado, la composición genérica permite la conexión de dos monikers, independientemente de sus clases. Por ejemplo, podría crear un moniker de elemento en un moniker de archivo, aunque no, por supuesto, al revés.

Dado que una composición no general depende de la clase de los monikers implicados, sus detalles se definen mediante la implementación de una clase de moniker determinada. Puede definir nuevos tipos de composiciones no genéricos si escribe una nueva clase de moniker. Por el contrario, OLE define las composiciones genéricas. Los monikers creados como resultado de la composición genérica se denominan monikers compuestos genéricos.

Estas tres clases, monikers de archivo, monikers de elementos y monikers compuestos genéricos, funcionan juntas y son las clases de monikers más usadas.

Los clientes de Moniker deben llamar a [**IMoniker::ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) para crear un compuesto en moniker con otro. El moniker en el que se llama internamente decide si puede realizar una composición genérica o no genérica. Si la implementación del moniker determina que se puede usar una composición genérica, OLE proporciona la [**función CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) para facilitar esto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti monikers](anti-monikers.md)
</dt> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[File Monikers](file-monikers.md)
</dt> <dt>

[Monikers de elementos](item-monikers.md)
</dt> <dt>

[Pointer Monikers](pointer-monikers.md)
</dt> </dl>

 

 




