---
title: Contenedores y servidores
description: Contenedores y servidores
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d301d85bc317cd4e60d609e73b6b7232cfb5634a33bf32a2496fe8cd672d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993575"
---
# <a name="containers-and-servers"></a>Contenedores y servidores

Las aplicaciones de documentos compuestos son de dos tipos básicos: aplicaciones de contenedor y aplicaciones de servidor. Las aplicaciones de contenedor OLE proporcionan a los usuarios la capacidad de crear, editar, guardar y recuperar documentos compuestos. Las aplicaciones de servidor OLE proporcionan a los usuarios los medios para crear documentos y otras representaciones de datos que se pueden incluir como vínculos o incrustaciones en aplicaciones de contenedor. Una aplicación OLE puede ser una aplicación contenedora, una aplicación de servidor o ambas.

Las aplicaciones de servidor OLE también difieren en si se implementan como servidores en *proceso o* como *servidores locales.* Un servidor en proceso es una biblioteca de vínculos dinámicos (DLL) que se ejecuta en el espacio de proceso de la aplicación contenedora. Puede ejecutar un servidor en proceso solo desde dentro de la aplicación contenedora.

> [!Note]  
> Las versiones futuras de OLE habilitarán la vinculación e inserción a través de los límites del equipo,  de modo que una aplicación contenedora en un equipo pueda usar un objeto de documento compuesto proporcionado por un servidor remoto que se ejecuta en otro equipo. Desde el punto de vista de una aplicación contenedora, cualquier aplicación de servidor OLE que se ejecute en su propio espacio de proceso, ya sea en el mismo equipo o en un equipo remoto, es un servidor fuera de *proceso.*

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> <dt>

[Servidores en proceso](in-process-servers.md)
</dt> </dl>

 

 




