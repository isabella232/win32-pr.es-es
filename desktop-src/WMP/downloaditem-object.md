---
title: Objeto DownloadItem
description: Objeto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player tiendas en línea, objeto DownloadItem
- tiendas en línea, objeto DownloadItem
- tipo 2 tiendas en línea, objeto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695472"
---
# <a name="downloaditem-object"></a>Objeto DownloadItem

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El objeto **DownloadItem** representa una solicitud de descarga de archivos. Las páginas web que se hospedan en el modo completo de Windows Media Player y que tienen acceso al objeto **externo** , como los servicios Premium, pueden usarlas.

El objeto **DownloadItem** admite las siguientes propiedades.



| Propiedad                                        | Descripción                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Recupera el estado de la descarga.             |
| [progreso](downloaditem-progress.md)           | Recupera el progreso de la descarga en bytes. |
| [size](downloaditem-size.md)                   | Recupera el tamaño de la descarga.              |
| [sourceURL](downloaditem-sourceurl.md)         | Recupera la dirección URL de origen de la descarga.        |
| [type](downloaditem-type.md)                   | Recupera el tipo de la descarga.              |



 

El objeto **DownloadItem** admite los siguientes métodos.



| Método                                      | Descripción                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Cancela la descarga.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Recupera el valor de un atributo para el elemento de descarga. |
| [pause](downloaditem-pause.md)             | Pausa la descarga.                                       |
| [Recuper](downloaditem-resume.md)           | Reanuda la descarga.                                      |



 

Se tiene acceso al objeto **DownloadItem** a través de la propiedad siguiente.



| Object                                              | Propiedad                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

A efectos de Ilustración, **Downloadmanager**. **getDownloadCollection**(*collectionId*). **Item**(*Itemid*) se usa en las secciones de sintaxis de referencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




