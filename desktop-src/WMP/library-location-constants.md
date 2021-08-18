---
title: Constantes de ubicación de biblioteca
description: Constantes de ubicación de biblioteca
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Reproductor de Windows Media en línea, constantes de ubicación de biblioteca
- tiendas en línea, constantes de ubicación de biblioteca
- tiendas en línea de tipo 1, constantes de ubicación de biblioteca
- Reproductor de Windows Media en línea, ubicaciones
- tiendas en línea, ubicaciones
- tipo 1 tiendas en línea, ubicaciones
- Reproductor de Windows Media biblioteca, constantes de ubicación
- library,location constants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a677f405ff36030647618a83bd0b8b952dae254a756cebc48e4c3210e5fcde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135368"
---
# <a name="library-location-constants"></a>Constantes de ubicación de biblioteca

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Las constantes de ubicación de la biblioteca son variables de cadena globales definidas en contentpartner.h. Se usan mediante determinados métodos de las interfaces [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) e [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) y por determinados métodos del [objeto External.](external-object-for-type-1-online-stores.md) Estas constantes se usan para indicar los tipos siguientes.

-   Tipo de ubicación de la biblioteca: este es el tipo de vista de biblioteca que muestra Reproductor de Windows Media. Por ejemplo, el reproductor podría mostrar una vista de un álbum determinado (g szCPAlbumID) o la vista de todos los \_ géneros (g \_ szAllCPGenreIDs).
-   Tipo de elemento seleccionado: este es el tipo de elemento seleccionado en la vista de biblioteca. Por ejemplo, el usuario podría seleccionar un álbum determinado (g \_ szCPAlbumID) en la vista de todos los discos.
-   Tipo de lista: este es el tipo de lista que se solicita desde el complemento del asociado de contenido. Por ejemplo, Reproductor de Windows Media podría pedir al complemento que proporcione una lista de elementos asociados a una lista de reproducción determinada (g \_ szCPListID).
-   Tipo de elemento de lista: el tipo de elemento de lista individual que se solicita desde el complemento del asociado de contenido. Por ejemplo, Reproductor de Windows Media podría pedir al complemento que proporcione la lista de pistas (g \_ szCPTrackID) en una lista de reproducción determinada.

En la tabla siguiente se proporciona el nombre y el valor de cada constante y una breve descripción de la ubicación o el tipo de la biblioteca. En el código de C o C++ que se compila con el archivo de encabezado contentpartner.h, puede usar el nombre o el valor de una constante. Es preferible usar el nombre porque el compilador detectará errores ortográficos. En el script (por ejemplo, al llamar a los métodos del [objeto External),](external-object-for-type-1-online-stores.md) no se puede usar el nombre de una constante; debe usar el valor .



| Nombre                              | Value                        | Ubicación o tipo                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | UnknownLocation              | Un conjunto de pistas que no es un álbum ni una lista de reproducción. Reproductor de Windows Media usa esta constante en el caso excepcional de que no puede determinar una ubicación válida. |
| g \_ szRootLocation                 | RootLocation                 | Nodo superior del control de vista de árbol de biblioteca                                                                                                                      |
| g \_ szFlyoutMenu                   | FlyoutMenu                   | Menú de salida de la tienda en línea actual                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | Todas las tiendas en línea                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | Una lista individual                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | Todas las listas                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | Una pista individual                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | Todas las pistas                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | Un intérprete individual                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | Todos los intérpretes                                                                                                                                                        |
| g \_ szCPAlbumID                    | CPAlbumID                    | Un álbum individual                                                                                                                                                |
| g \_ szAllCPAlbumIDs                | AllCPAlbumIDs                | Todos los discos                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | Un género individual                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | Todos los géneros                                                                                                                                                         |
| g \_ szCPAlbumSubGenreID            | CPAlbumSubGenreID            | Un subgéneo individual                                                                                                                                             |
| g \_ szAllCPAlbumSubGenreIDs        | AllCPAlbumSubGenreIDs        | Todos los subgéneos                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | Año individual en el que se publicó el contenido del catálogo                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | Todos los años que se publicó el contenido del catálogo                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | Una secuencia de radio individual                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | Todas las secuencias de radio                                                                                                                                                  |
| g \_ szAuthor                       | Autor                       | Un autor individual                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | Todos los autores                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | Una clasificación parental individual                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | Todas las clasificaciones parentales                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | Una clasificación de usuario individual, medida como un número de estrellas                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | Todas las clasificaciones de usuario                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External.addToBasket**](external-addtobasket.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**External.changeView**](external-changeview.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.download**](external-download.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner::GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner::InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




