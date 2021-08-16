---
title: DownloadManager (objeto)
description: DownloadManager (objeto)
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Reproductor de Windows Media en línea, objeto DownloadManager
- tiendas en línea, objeto DownloadManager
- tipo 2 tiendas en línea, objeto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 500061e414d7321ed6fe4c46cafc79cd6795935847bb3d8c527364497722ecf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340529"
---
# <a name="downloadmanager-object"></a>DownloadManager (objeto)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **objeto DownloadManager** es el objeto raíz del administrador Reproductor de Windows Media descarga. Las páginas web que se hospedan en los paneles de tareas del servicio de la tienda en línea pueden usarla.

El **objeto DownloadManager** admite los métodos siguientes.



| Método                                                                   | Descripción                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Crea una colección de descarga vacía.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Recupera la colección de descarga especificada. |



 

Se tiene acceso al objeto **DownloadManager** mediante **external. DownloadManager**. Con fines ilustrativos, se supone que este valor se ha asignado a una variable denominada "DownloadManager", que se usará para identificar este objeto en las secciones de sintaxis de referencia.

En Reproductor de Windows Media 10 o posterior, la propiedad **DownloadManager** y el objeto solo son accesibles desde los paneles de tareas del servicio de la tienda en línea. No se puede usar **DownloadManager desde otras** características en las que el **objeto** Externo está disponible, como HTMLView, vista del centro de información e información del álbum.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




