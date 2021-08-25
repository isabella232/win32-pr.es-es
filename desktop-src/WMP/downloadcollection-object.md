---
title: DownloadCollection (objeto)
description: DownloadCollection (objeto)
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Reproductor de Windows Media en línea, objeto DownloadCollection
- online stores,DownloadCollection (objeto)
- tipo 2 tiendas en línea, objeto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565ddce120d71ab9825c424fefb6f0e3ace9a6ac349e87e044e9c74e6da28789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902025"
---
# <a name="downloadcollection-object"></a>DownloadCollection (objeto)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **objeto DownloadCollection** contiene propiedades y métodos para controlar colecciones de elementos de descarga. Se puede usar en páginas web hospedadas en el modo completo Reproductor de Windows Media  y que tienen acceso al objeto Externo, como las tiendas en línea.

El **objeto DownloadCollection** admite las siguientes propiedades.



| Propiedad                              | Descripción                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Recupera el número de descargas pendientes.   |
| [identificador](downloadcollection-id.md)       | Recupera el identificador de la colección de descarga. |



 

El **objeto DownloadCollection** admite los métodos siguientes.



| Método                                                | Descripción                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Borrar](downloadcollection-clear.md)                 | Quita todos los elementos de una colección de descarga. |
| [item](downloadcollection-item.md)                   | Recupera un objeto de descarga pendiente.          |
| [removeItem](downloadcollection-removeitem.md)       | Quita un elemento de descarga de una colección.    |
| [startDownload](downloadcollection-startdownload.md) | Pone en cola una descarga.                            |



 

Se **accede al objeto DownloadCollection** a través de los métodos siguientes.



| Object                                        | Método                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

Para fines ilustrativos, **DownloadManager**. **getDownloadCollection**(*collectionId*) se usa en las secciones de sintaxis de referencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




