---
title: Música Catálogo
description: Música Catálogo
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Reproductor de Windows Media en línea, catálogos de música
- tiendas en línea, catálogos de música
- tiendas en línea de tipo 1, catálogos de música
- Reproductor de Windows Media en línea,compilador de catálogo
- tiendas en línea, compilador de catálogos
- tiendas en línea de tipo 1, compilador de catálogo
- catálogos de música
- compilador de catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359280"
---
# <a name="music-catalog"></a>Música Catálogo

Una tienda en línea de tipo 1 crea su catálogo de música como un conjunto de archivos de valores separados por tabulaciones (TSV). A continuación, la [](catalog-compiler-for-type-1-online-stores.md) tienda en línea usa el compilador de catálogos de Microsoft para compilar los archivos TSV en un catálogo comprimido que puede descargar Reproductor de Windows Media. Reproductor de Windows Media puede descargar archivos de catálogo completos o archivos de actualización de catálogo. Las actualizaciones de catálogo contienen solo la información del catálogo que ha cambiado desde la última actualización del catálogo. Es el complemento de asociado de contenido el que determina si se debe descargar un catálogo completo o una actualización. En cualquier caso, Reproductor de Windows Media aplica los cambios al catálogo actual tras la notificación desde el complemento.

Si la tienda en línea tiene preparado un nuevo catálogo, el complemento puede notificar al reproductor llamando a [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) y pasando wmpcnNewCatalogAvailable como valor para el parámetro de tipo. 

Cuando Reproductor de Windows Media está listo para descargar un catálogo o actualización, el reproductor llama a [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). Este método proporciona al complemento información sobre el catálogo actual, como la versión del catálogo y el identificador de configuración regional. El complemento responde al proporcionar el localizador uniforme de recursos (URL) del catálogo completo o la actualización correctos, así como un número de versión actualizado y la fecha de expiración. Reproductor de Windows Media solicitudes periódicas de actualizaciones del catálogo en función de la información proporcionada por el complemento en **GetCatalogURL**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Compilador de catálogos para almacenes en línea de tipo 1**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner (interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




