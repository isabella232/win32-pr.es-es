---
title: Objetos vinculados y monikers
description: Los objetos vinculados, como los objetos incrustados, se basan en un controlador de objetos para comunicarse con las aplicaciones de servidor.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249291"
---
# <a name="linked-objects-and-monikers"></a>Objetos vinculados y monikers

Los objetos vinculados, como los objetos incrustados, se basan en un controlador de objetos para comunicarse con las aplicaciones de servidor. Sin embargo, el propio objeto vinculado administra la nomenclatura y el seguimiento de los orígenes de vínculos. El objeto vinculado actúa como un servidor en proceso. Por ejemplo, cuando se activa, un objeto vinculado busca e inicia la aplicación de servidor OLE que es el origen del vínculo.

El controlador de un objeto vinculado se forma de dos componentes principales: el componente de controlador y el componente de vinculación. El componente de controlador contiene las partes y funciones de control y comunicación remota muy similares a un controlador para un objeto incrustado. El componente de vinculación tiene su propio controlador y caché y proporciona acceso al almacenamiento estructurado del objeto. El controlador de componentes de vinculación admite la nomenclatura de origen mediante el uso de monikers y el enlace, el proceso de buscar y ejecutar el origen del vínculo. (Para obtener más información sobre los monikers y el enlace, vea [El modelo de objetos componentes](the-component-object-model.md)).

Cuando un usuario crea inicialmente un objeto vinculado o carga uno existente desde el almacenamiento, el contenedor carga una instancia del componente de vinculación en la memoria, junto con el controlador de objetos. El componente de vinculación proporciona interfaces , especialmente [**IOleLink,**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)que identifican el objeto como un vínculo y le permiten administrar la nomenclatura, el seguimiento y la actualización de su origen de vínculo.

Al implementar la [**interfaz IOleLink,**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) un objeto vinculado proporciona a su contenedor funciones que admiten la vinculación. Solo los objetos vinculados **implementan IOleLink** y, al consultar esta interfaz, un contenedor puede determinar si un objeto determinado está incrustado o vinculado. La función más importante proporcionada por **IOleLink** permite a un contenedor enlazar al origen del objeto vinculado, es decir, activar la conexión al documento que almacena los datos nativos del objeto vinculado. **IOleLink también** define funciones para administrar información sobre el objeto vinculado, como los datos de presentación almacenados en caché y la ubicación del origen del vínculo.

Cuando se guarda un documento compuesto que contiene un objeto vinculado, los datos del vínculo se guardan con el origen del vínculo, no con el contenedor. Solo se guarda información sobre su nombre y ubicación junto con el documento compuesto. Este comportamiento contrasta con el de un objeto incrustado, cuyos datos se almacenan junto con el de su contenedor.

Las aplicaciones de contenedor pueden proporcionar información sobre sus objetos incrustados, de forma que estos últimos, o partes de los mismos, pueden actuar como orígenes de vínculo. Al implementar la compatibilidad con la vinculación a los objetos incrustados del contenedor, puede hacer posibles inserciones anidadas, lo que ayuda al usuario a tener que realizar un seguimiento de los originales de cada objeto de inserción al que se desea un vínculo. Por ejemplo, si un usuario desea insertar una hoja de cálculo de Microsoft Excel en Microsoft Word y la hoja de cálculo contiene un mapa de bits creado en Paintbrush, el usuario puede vincular a una copia del mapa de bits contenido en la hoja de cálculo en lugar del original.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> <dt>

[Servidores en proceso](in-process-servers.md)
</dt> <dt>

[Controladores de objetos](object-handlers.md)
</dt> </dl>

 

 




