---
title: Objeto DownloadCollection
description: Objeto DownloadCollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player tiendas en línea, objeto DownloadCollection
- tiendas en línea, objeto DownloadCollection
- tipo 2 tiendas en línea, objeto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695388"
---
# <a name="downloadcollection-object"></a>Objeto DownloadCollection

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El objeto **DownloadCollection** contiene propiedades y métodos para controlar las colecciones de elementos de descarga. Las páginas web que se hospedan en el modo completo de Windows Media Player y que tienen acceso al objeto **externo** , como las tiendas en línea, pueden usarlas.

El objeto **DownloadCollection** admite las siguientes propiedades.



| Propiedad                              | Descripción                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Recupera el número de descargas pendientes.   |
| [id](downloadcollection-id.md)       | Recupera el identificador de la colección de descargas. |



 

El objeto **DownloadCollection** admite los siguientes métodos.



| Método                                                | Descripción                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Borrar](downloadcollection-clear.md)                 | Quita todos los elementos de una colección de descarga. |
| [item](downloadcollection-item.md)                   | Recupera un objeto de descarga pendiente.          |
| [removeItem](downloadcollection-removeitem.md)       | Quita un elemento de descarga de una colección.    |
| [startDownload](downloadcollection-startdownload.md) | Pone en cola una descarga.                            |



 

Se tiene acceso al objeto **DownloadCollection** a través de los métodos siguientes.



| Object                                        | Método                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

A efectos de Ilustración, **Downloadmanager**. **getDownloadCollection**(*collectionId*) se usa en las secciones de sintaxis de referencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




