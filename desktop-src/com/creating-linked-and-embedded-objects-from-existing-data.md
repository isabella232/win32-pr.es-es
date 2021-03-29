---
title: Crear objetos vinculados e incrustados a partir de datos existentes
description: Crear objetos vinculados e incrustados a partir de datos existentes
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779801"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a>Crear objetos vinculados e incrustados a partir de datos existentes

Normalmente, un usuario ensambla un documento compuesto con el portapapeles o con arrastrar y colocar para copiar un objeto de datos de su aplicación de servidor en la aplicación contenedora del usuario. Con las aplicaciones que admiten OLE, el usuario puede iniciar la transferencia desde el servidor o el contenedor. Por ejemplo, el servidor puede copiar datos en el portapapeles en la aplicación de servidor, cambiar a la aplicación contenedora y elegir pegar un objeto especial o incrustado o un comando de menú equivalente para crear un nuevo objeto incrustado a partir de los datos seleccionados. O bien, el usuario puede arrastrar los datos de una aplicación al otro. El proceso es similar para crear un objeto vinculado.

> [!Note]  
> Una aplicación que funciona como servidor OLE y como contenedor puede utilizar una selección de sus propios datos para crear un objeto incrustado o vinculado en una nueva ubicación dentro del mismo documento.

 

La transferencia de datos entre el servidor OLE y las aplicaciones de contenedor se basa en la transferencia de datos uniforme, como se describe en [transferencia de datos](data-transfer.md). Los servidores OLE y los controladores de objetos implementan [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para que sus datos estén disponibles para las transferencias mediante el portapapeles o arrastrar y colocar. Los objetos OLE admiten todos los formatos de Portapapeles habituales. Además, admiten seis formatos del portapapeles que admiten la creación de objetos vinculados e incrustados a partir de un objeto de datos seleccionado.

Los formatos del portapapeles OLE describen objetos de datos que, al colocarse o pegarse en contenedores OLE, se convertirán en objetos de documento compuesto incrustados o vinculados. El objeto de datos presenta estos formatos a las aplicaciones de contenedor en orden de fidelidad como descripciones de los datos. En otras palabras, el objeto presenta primero el formato que mejor lo representa, seguido del siguiente formato mejor, etc. Esta ordenación intencional fomenta que una aplicación contenedora use el mejor formato posible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

 




