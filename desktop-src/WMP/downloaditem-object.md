---
title: DownloadItem (objeto)
description: DownloadItem (objeto)
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Reproductor de Windows Media en línea, objeto DownloadItem
- online stores,DownloadItem (objeto)
- tipo 2 tiendas en línea, objeto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfea6241e81352b8848304c3601650ef4dec2a8e5692874fa20995ccddcce38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863465"
---
# <a name="downloaditem-object"></a>DownloadItem (objeto)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **objeto DownloadItem** representa una solicitud de descarga de archivos. Se puede usar en páginas web que se hospedan en el modo  completo Reproductor de Windows Media y que tienen acceso al objeto Externo, como los servicios Premium.

El **objeto DownloadItem** admite las siguientes propiedades.



| Propiedad                                        | Descripción                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Recupera el estado de la descarga.             |
| [Progreso](downloaditem-progress.md)           | Recupera el progreso de la descarga en bytes. |
| [size](downloaditem-size.md)                   | Recupera el tamaño de la descarga.              |
| [sourceURL](downloaditem-sourceurl.md)         | Recupera la dirección URL de origen de la descarga.        |
| [type](downloaditem-type.md)                   | Recupera el tipo de la descarga.              |



 

El **objeto DownloadItem** admite los métodos siguientes.



| Método                                      | Descripción                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Cancela la descarga.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Recupera el valor de un atributo para el elemento de descarga. |
| [pause](downloaditem-pause.md)             | Pausa la descarga.                                       |
| [Reanudar](downloaditem-resume.md)           | Reanuda la descarga.                                      |



 

Se tiene acceso al objeto **DownloadItem** a través de la propiedad siguiente.



| Object                                              | Propiedad                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

Para fines ilustrativos, **DownloadManager**. **getDownloadCollection**(*collectionId*). **item**(*itemId*) se usa en las secciones de sintaxis de referencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




