---
title: Objeto DownloadManager
description: Objeto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player tiendas en línea, objeto DownloadManager
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
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903575"
---
# <a name="downloadmanager-object"></a>Objeto DownloadManager

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El objeto **Downloadmanager** es el objeto raíz para el administrador de descargas de Windows Media Player. Lo pueden usar las páginas web que se hospedan en los paneles de tareas de servicio de tienda en línea.

El objeto **Downloadmanager** admite los siguientes métodos.



| Método                                                                   | Descripción                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Crea una colección de descargas vacía.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Recupera la colección de descarga especificada. |



 

Se tiene acceso al objeto **Downloadmanager** mediante **external. DownloadManager**. A efectos de Ilustración, se supone que este valor se ha asignado a una variable denominada "DownloadManager", que se usará para identificar este objeto en las secciones de sintaxis de referencia.

En Windows Media Player 10 o versiones posteriores, solo se puede tener acceso a la propiedad y el objeto **Downloadmanager** desde los paneles de tareas servicio de tienda en línea. No se puede usar el **Downloadmanager** de otras características en las que el objeto **externo** está disponible, como HTMLView, la vista del centro de información y la información del álbum.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




