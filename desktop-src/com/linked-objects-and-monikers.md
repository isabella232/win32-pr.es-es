---
title: Objetos y monikers vinculados
description: Los objetos vinculados, como los objetos incrustados, dependen de un controlador de objetos para comunicarse con las aplicaciones de servidor.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269281"
---
# <a name="linked-objects-and-monikers"></a>Objetos y monikers vinculados

Los objetos vinculados, como los objetos incrustados, dependen de un controlador de objetos para comunicarse con las aplicaciones de servidor. Sin embargo, el propio objeto vinculado administra la nomenclatura y el seguimiento de los orígenes de vínculo. El objeto vinculado actúa como un servidor en proceso. Por ejemplo, cuando se activa, un objeto vinculado localiza e inicia la aplicación de servidor OLE que es el origen del vínculo.

El controlador de un objeto vinculado se compone de dos componentes principales: el componente de controlador y el componente de vinculación. El componente de controlador contiene el control y las partes de la comunicación remota y las funciones de forma muy similar a un controlador para un objeto incrustado. El componente de vinculación tiene su propio controlador y caché, y proporciona acceso al almacenamiento estructurado del objeto. El controlador de componentes de vinculación admite la asignación de nombres de origen mediante el uso de monikers y el enlace, el proceso de búsqueda y ejecución del origen del vínculo. (Para obtener más información acerca de los monikers y el enlace, vea [el modelo de objetos componentes](the-component-object-model.md)).

Cuando un usuario crea inicialmente un objeto vinculado o carga uno existente desde el almacenamiento, el contenedor carga una instancia del componente de vinculación en la memoria, junto con el controlador de objetos. El componente de vinculación proporciona interfaces (especialmente [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)) que identifican el objeto como un vínculo y permiten administrar la nomenclatura, el seguimiento y la actualización de su origen de vínculo.

Mediante la implementación de la interfaz [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) , un objeto vinculado proporciona a su contenedor funciones que admiten la vinculación. Solo los objetos vinculados implementan **IOleLink** y al consultar esta interfaz, un contenedor puede determinar si un objeto determinado está incrustado o vinculado. La función más importante proporcionada por **IOleLink** permite a un contenedor enlazarse al origen del objeto vinculado, es decir, para activar la conexión al documento que almacena los datos nativos del objeto vinculado. **IOleLink** también define funciones para administrar información sobre el objeto vinculado, como los datos de presentación almacenados en caché y la ubicación del origen del vínculo.

Cuando se guarda un documento compuesto que contiene un objeto vinculado, los datos del vínculo se guardan con el origen del vínculo, no con el contenedor. Solo se guarda información sobre su nombre y ubicación junto con el documento compuesto. Este comportamiento es diferente al de un objeto incrustado, cuyos datos se almacenan junto con el de su contenedor.

Las aplicaciones contenedoras pueden proporcionar información sobre sus objetos incrustados, de modo que el último, o partes de ellos, pueden actuar como orígenes de vínculo. Mediante la implementación de la compatibilidad para la vinculación a los objetos incrustados del contenedor, es posible realizar incrustaciones anidadas, lo que evita que el usuario tenga que realizar un seguimiento de los originales de cada objeto de incrustación al que se desea un vínculo. Por ejemplo, si un usuario desea incrustar una hoja de cálculo de Microsoft Excel en Microsoft Word y la hoja de cálculo contiene un mapa de bits creado en Paintbrush, el usuario puede crear un vínculo a una copia del mapa de bits incluido en la hoja de cálculo en lugar del original.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> <dt>

[Servidores en proceso](in-process-servers.md)
</dt> <dt>

[Controladores de objetos](object-handlers.md)
</dt> </dl>

 

 




