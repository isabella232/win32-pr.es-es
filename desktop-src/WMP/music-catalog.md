---
title: Catálogo de música
description: Catálogo de música
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player tiendas en línea, catálogos de música
- tiendas en línea, catálogos de música
- tipo 1 almacenes en línea, catálogos de música
- Windows Media Player tiendas en línea, compilador de catálogos
- tiendas en línea, compilador de catálogos
- tipo 1 almacenes en línea, compilador de catálogos
- catálogos de música
- compilador de catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077286"
---
# <a name="music-catalog"></a>Catálogo de música

Un almacén en línea de tipo 1 crea su catálogo de música como un conjunto de archivos de valores separados por tabulaciones (TSV). A continuación, la tienda en línea usa el [compilador de catálogo](catalog-compiler-for-type-1-online-stores.md) de Microsoft para compilar los archivos TSV en un catálogo comprimido que se puede descargar mediante Windows Media Player. Windows Media Player puede descargar archivos de catálogo completos o archivos de actualización de catálogo. Las actualizaciones del catálogo solo contienen la información del catálogo que ha cambiado desde la última actualización del catálogo. Es el complemento de asociado de contenido el que determina si se debe descargar un catálogo completo o una actualización. En cualquier caso, Windows Media Player aplica los cambios al catálogo actual después de la notificación del complemento.

Si la tienda en línea tiene un catálogo nuevo preparado, el complemento puede notificar al reproductor llamando a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) y pasando wmpcnNewCatalogAvailable como valor para el parámetro de *tipo* .

Cuando Windows Media Player está listo para descargar un catálogo o una actualización, el reproductor llama a [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). Este método proporciona al complemento información sobre el catálogo actual, como la versión del catálogo y el identificador de configuración regional. El complemento responde proporcionando el localizador uniforme de recursos (URL) de la actualización o el catálogo completo correctos, así como un número de versión actualizado y una fecha de expiración. Windows Media Player solicitará periódicamente actualizaciones de catálogo basadas en la información proporcionada por el complemento en **GetCatalogURL**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Compilador de catálogo para las tiendas en línea de tipo 1**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**Interfaz IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




