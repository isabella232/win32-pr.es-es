---
title: Monikers compuestos
description: Una de las características más útiles de monikers es que se pueden concatenar o componer monikers juntos.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5375bb505ff3737fb4e0cdea894790d93c0051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779812"
---
# <a name="composite-monikers"></a>Monikers compuestos

Una de las características más útiles de monikers es que se pueden concatenar o componer monikers juntos. Un *moniker compuesto* es un moniker que es una composición de otros monikers y puede determinar la relación entre los elementos. Esto le permite ensamblar la ruta de acceso completa a un objeto, dados dos o más monikers equivalentes a los trazados parciales. Puede crear monikers de la misma clase (como dos monikers de archivo) o de clases diferentes (como un moniker de archivo y un moniker de elemento). Si va a escribir su propia clase moniker, también puede crear sus monikers con monikers de archivo o elemento. La ventaja básica de un compuesto es que proporciona un fragmento de código para implementar cada moniker posible que es una combinación de monikers más simples. Esto reduce significativamente la necesidad de clases de moniker personalizadas específicas.

Dado que los monikers de clases diferentes pueden estar compuestos entre sí, los monikers proporcionan la capacidad de combinar varios espacios de nombres. El sistema de archivos define un espacio de nombres común para los objetos almacenados como archivos, ya que todas las aplicaciones entienden el nombre de la ruta de acceso del sistema de archivos. Del mismo modo, un objeto contenedor también define un espacio de nombres privado para los objetos que contiene porque ningún contenedor entiende los nombres generados por otro contenedor. Los monikers permiten combinar estos espacios de nombres porque se pueden componer monikers de archivo y monikers de elemento. Un cliente de moniker puede buscar en el espacio de nombres todos los objetos que usan un único mecanismo. El cliente simplemente llama a [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en el moniker y el código de moniker controla el resto. Una llamada a [**IMoniker:: getDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) en un compuesto crea un nombre mediante la concatenación de todos los nombres para mostrar de los monikers individuales.

Además, dado que puede escribir su propia clase de moniker, la composición de moniker le permite agregar extensiones personalizadas al espacio de nombres para los objetos.

A veces, se pueden combinar dos monikers de clases específicas de una manera especial. Por ejemplo, un moniker de archivo que representa una ruta de acceso incompleta y otro que representa una ruta de acceso relativa se puede combinar para formar un solo moniker de archivo que represente la ruta de acceso completa. Por ejemplo, los monikers de archivo "c: \\ Work \\ Art" pueden estar compuestos con el moniker de archivo relativo ".. \\ \\myfile.doc de copia de seguridad "para que sea igual a" c: \\ copia de seguridad de trabajo \\ \\myfile.doc ". Este es un ejemplo de *composición no genérica*.

La *composición genérica*, por otro lado, permite la conexión de dos monikers cualesquiera, independientemente de cuáles sean sus clases. Por ejemplo, podría crear un moniker de elemento en un moniker de archivo, aunque no, por supuesto, de otra manera.

Dado que una composición no genérica depende de la clase de los monikers implicados, sus detalles se definen mediante la implementación de una clase de moniker determinada. Puede definir nuevos tipos de composiciones no genéricas si escribe una nueva clase de moniker. Por el contrario, OLE define las composiciones genéricas. Los monikers creados como resultado de la composición genérica se denominan monikers compuestos genéricos.

Estas tres clases, monikers de archivo, monikers de elemento y monikers compuestos genéricos, funcionan conjuntamente y son las clases de monikers que se usan con más frecuencia.

Los clientes moniker deben llamar a [**IMoniker:: ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) para crear una composición en el moniker con otro. El moniker al que se llama internamente decide si puede realizar una composición genérica o no genérica. Si la implementación de moniker determina que se puede usar una composición genérica, OLE proporciona la función [**CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) para facilitar esto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de elemento](item-monikers.md)
</dt> <dt>

[Monikers de puntero](pointer-monikers.md)
</dt> </dl>

 

 




