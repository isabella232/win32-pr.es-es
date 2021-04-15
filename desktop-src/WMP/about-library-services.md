---
title: Acerca de los servicios de biblioteca
description: Acerca de los servicios de biblioteca
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, acerca de
- Biblioteca de Media Player de Windows, servicios
- Biblioteca, servicios
- Biblioteca, acerca de
- versiones de Windows Media Player, servicios de biblioteca
- enumeraciones, servicios de biblioteca
- eventos, servicios de biblioteca
- ejemplos, servicios de biblioteca
- interfaces, servicios de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743efc8ae5cb464aa38655314c52112bc9541de6
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105695568"
---
# <a name="about-library-services"></a>Acerca de los servicios de biblioteca

En versiones anteriores de Windows Media Player, el software usaba una sola base de datos de biblioteca para cada usuario. Esta base de datos se almacenó en el equipo del usuario y estaba relacionada conceptualmente con el usuario y con una instancia determinada del reproductor.

Windows Media Player 11 presenta los conceptos de varias bibliotecas remotas y. Ahora, además de su biblioteca predeterminada, o *local*, Windows Media Player puede mostrar el contenido recuperado de las bibliotecas en otros equipos conectados a una red, lo que puede incluir otros usuarios que han iniciado sesión en el mismo equipo. El reproductor también puede mostrar vistas de biblioteca de otros orígenes, como dispositivos habilitados para MTP o CDs de datos. Desde la perspectiva del usuario final, esto significa que el contenido multimedia digital que se encuentra en muchos lugares diferentes puede administrarse desde varias ubicaciones mediante la misma interfaz de usuario conocida de Windows Media Player. Desde la perspectiva del desarrollador, esto significa que puede usar las interfaces COM del SDK de Windows Media Player para enumerar las bibliotecas disponibles y, a continuación, utilizarlas como si usara la biblioteca local en versiones anteriores.

Para enumerar las bibliotecas disponibles, use la interfaz **IWMPLibraryServices** . Esta interfaz expone el método [IWMPLibraryServices:: getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) , que recupera el recuento de bibliotecas de un tipo determinado. Los tipos de biblioteca se definen mediante la enumeración [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) . Esta enumeración incluye un valor para la biblioteca local, wmpltLocal. Esto se debe a que la característica servicios de biblioteca siempre permite trabajar con la biblioteca local mediante **IWMPLibraryServices** y las interfaces relacionadas.

> [!Note]  
> La enumeración **WMPLibraryType** incluye el valor wmpltRemote, que representa las bibliotecas multimedia compartidas por la red. Para tener acceso a esas bibliotecas compartidas, el control Player debe estar ejecutándose en modo remoto. Para obtener información sobre cómo ejecutar el control Player en el modo remoto, vea [Remoting The Windows Media Player control](remoting-the-windows-media-player-control.md).

 

Después de recuperar el número de bibliotecas, puede recorrer en iteración la colección de bibliotecas disponibles mediante una llamada repetida a [IWMPLibraryServices:: getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) en un bucle, pasando un nuevo valor de índice con cada iteración. Este método recupera un puntero a una interfaz [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) , que representa la biblioteca individual.

Después de recuperar un puntero a **IWMPLibrary**, puede llamar a [IWMPLibrary:: get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) para recuperar un puntero a una interfaz **IWMPMediaCollection** . Con este puntero de interfaz, puede trabajar con una biblioteca individual de forma muy similar a como usaría la biblioteca local. También puede recuperar una cadena que contiene el nombre de la biblioteca mediante una llamada a [IWMPLibrary:: get \_ Name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), que es útil si necesita mostrar el nombre de la biblioteca al usuario. Puede llamar a [IWMPLibrary:: get \_ Type](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) para obtener el **WMPLibraryType** de una biblioteca determinada.

Puede controlar el evento [IWMPEvents3:: LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) para saber cuándo está disponible una biblioteca y el evento [IWMPEvents3:: LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) para saber cuándo se desconecta una biblioteca. Cada uno de estos eventos proporciona un puntero **IWMPLibrary** que representa la biblioteca que se conectó o se desconectó. Puede llamar a [IWMPLibrary:: isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) para determinar si la biblioteca que se conectó o desconectó es una biblioteca que está usando actualmente.

Hay algunas diferencias importantes cuando se trabaja con una biblioteca recuperada a través de la interfaz **IWMPLibraryServices** en comparación con el uso de una biblioteca recuperada mediante [IWMPCore:: get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection). Se aplican las diferencias siguientes:

-   Normalmente, puede recuperar los resultados de la consulta mucho más rápido de las bibliotecas recuperadas a través de **IWMPLibraryServices**. (Esto supone que otros factores, como los tiempos de acceso de red y disco duro, son iguales).
-   La lista de atributos de metadatos de elementos multimedia disponibles en las bibliotecas recuperadas a través de **IWMPLibraryServices** suele ser un subconjunto de los que están disponibles en la biblioteca local recuperada a través de [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore).
-   Si recupera la biblioteca local a través de **IWMPLibraryServices**, todos los mismos atributos están disponibles para su uso como los que están disponibles al recuperar la biblioteca local a través de **IWMPCore**. Sin embargo, podrá recuperar los resultados de la consulta mucho más rápido para los atributos de uso más frecuente.
-   Debe usar colecciones de cadenas para crear elementos de la interfaz de usuario al trabajar con las bibliotecas recuperadas a través de **IWMPLibraryServices**. Por ejemplo, [IWMPMediaCollection2:: getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) permite usar una consulta personalizada (representada por la interfaz **IWMPQuery** ) para recuperar una colección de cadenas.
-   Es posible que las bibliotecas remotas recuperadas a través de la interfaz **IWMPLibraryServices** no siempre estén conectadas a la instancia actual del reproductor. Esto significa que es importante controlar los eventos **LibraryConnect** y **LibraryDisconnect** para saber cuándo cambia la disponibilidad de la biblioteca y controlar el evento [IWMPEvents3:: StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) para saber cuándo se agregan o quitan cadenas de las colecciones de cadenas que se usan para mostrar los elementos de la interfaz de usuario. También debe controlar los eventos de **StringCollectionChange** para la biblioteca local por motivos similares.

Es importante comprender que las colecciones de cadenas de una biblioteca determinada pueden cambiar en cualquier momento. Una colección de cadenas puede estar vacía cuando se recupera por primera vez, como en el caso de una biblioteca que se ha conectado recientemente pero el reproductor todavía no ha enumerado su contenido. Por el contrario, es posible que una colección de cadenas ya contenga toda la información que necesita. En este caso, es posible que nunca reciba un evento **StringCollectionChange** porque el contenido de la biblioteca se ha enumerado completamente antes de crear la consulta y no está cambiando nada más.

Por lo tanto, para mantener la interfaz de usuario actual, debe enumerar el contenido de la colección de cadenas al recuperar la interfaz **IWMPStringCollection** y controlar el evento **StringCollectionChange** para conocer las actualizaciones cuando se producen.

## <a name="sample"></a>Muestra

En el ejemplo denominado WMPML se muestra cómo trabajar con servicios de biblioteca. Para obtener más información acerca de los ejemplos del SDK de Windows Media Player, vea [ejemplos](samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la biblioteca**](about-the-library.md)
</dt> <dt>

[**Acerca del objeto de consulta**](about-the-query-object.md)
</dt> <dt>

[**Interfaz IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interfaz IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




