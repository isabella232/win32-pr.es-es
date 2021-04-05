---
title: Constantes de ubicación de biblioteca
description: Constantes de ubicación de biblioteca
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player tiendas en línea, constantes de ubicación de biblioteca
- tiendas en línea, constantes de ubicación de biblioteca
- tipo 1 almacenes en línea, constantes de ubicación de biblioteca
- Windows Media Player tiendas en línea, ubicaciones
- tiendas en línea, ubicaciones
- tipo 1 almacenes en línea, ubicaciones
- Biblioteca de Media Player de Windows, constantes de ubicación
- Biblioteca, constantes de ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cbb297831acce9724988309880390cdcbe1894
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420448"
---
# <a name="library-location-constants"></a>Constantes de ubicación de biblioteca

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Las constantes de ubicación de biblioteca son variables de cadena globales definidas en contentpartner. h. Los utilizan ciertos métodos de las interfaces [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) y [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) , así como ciertos métodos del objeto [externo](external-object-for-type-1-online-stores.md) . Estas constantes se utilizan para indicar los tipos siguientes.

-   Tipo de ubicación de la biblioteca: es el tipo de vista de biblioteca que se muestra en Windows Media Player. Por ejemplo, es posible que el reproductor muestre una vista de un álbum determinado (g \_ szCPAlbumID) o la vista de todos los géneros (g \_ szAllCPGenreIDs).
-   Tipo de elemento seleccionado: este es el tipo de elemento seleccionado en la vista biblioteca. Por ejemplo, el usuario podría seleccionar un álbum determinado (g \_ szCPAlbumID) en la vista de todos los álbumes.
-   Tipo de lista: este es el tipo de lista que se solicita desde el complemento de asociado de contenido. Por ejemplo, Windows Media Player podría pedir al complemento que proporcione una lista de elementos asociados a una lista de reproducción determinada (g \_ szCPListID).
-   Tipo de elemento de lista: el tipo de elemento de lista individual que se solicita desde el complemento de asociado de contenido. Por ejemplo, Windows Media Player podría pedir al complemento que proporcione la lista de pistas (g \_ szCPTrackID) en una lista de reproducción determinada.

En la tabla siguiente se proporciona el nombre y el valor de cada constante y una breve descripción de la ubicación o el tipo de la biblioteca. En código de C o C++ que se compila con el archivo de encabezado contentpartner. h, se puede usar el nombre o el valor de una constante. Es preferible usar el nombre porque el compilador detectará errores ortográficos. En el script (por ejemplo, al llamar a los métodos del objeto [externo](external-object-for-type-1-online-stores.md) ), no puede utilizar el nombre de una constante; debe utilizar el valor.



| Nombre                              | Value                        | Ubicación o tipo                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | UnknownLocation              | Un conjunto de pistas que no es un álbum ni una lista de reproducción. Windows Media Player también usa esta constante en el caso excepcional de que no pueda determinar una ubicación válida. |
| g \_ szRootLocation                 | RootLocation                 | Nodo superior del control de vista de árbol de la biblioteca                                                                                                                      |
| g \_ szFlyoutMenu                   | FlyoutMenu                   | Menú de control flotante de la tienda en línea actual                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | Todas las tiendas en línea                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | Una lista individual                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | Todas las listas                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | Una pista individual                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | Todas las pistas                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | Un intérprete individual                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | Todos los artistas                                                                                                                                                        |
| g \_ szCPAlbumID                    | CPAlbumID                    | Un álbum individual                                                                                                                                                |
| g \_ szAllCPAlbumIDs                | AllCPAlbumIDs                | Todos los álbumes                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | Un género individual                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | Todos los géneros                                                                                                                                                         |
| g \_ szCPAlbumSubGenreID            | CPAlbumSubGenreID            | Un subgénero individual                                                                                                                                             |
| g \_ szAllCPAlbumSubGenreIDs        | AllCPAlbumSubGenreIDs        | Todos los subgéneros                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | Un año individual en el que se liberó el contenido del catálogo                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | Todos los años en los que se liberó el contenido del catálogo                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | Un flujo de radio individual                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | Todas las secuencias de radio                                                                                                                                                  |
| g \_ szAuthor                       | Autor                       | Un autor individual                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | Todos los autores                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | Una clasificación parental individual                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | Todas las clasificaciones parentales                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | Una clasificación de usuario individual, medida como un número de estrellas                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | Todas las clasificaciones de usuario                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External. addToBasket**](external-addtobasket.md)
</dt> <dt>

[**External. Buy**](external-buy.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. download**](external-download.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. Play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner::GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner:: InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




