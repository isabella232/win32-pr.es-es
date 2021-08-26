---
title: Acerca de Los servicios de biblioteca
description: Acerca de Los servicios de biblioteca
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media modelo de objetos,library
- object model,library
- Reproductor de Windows Media ActiveX control,library para el modelo de objetos
- ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,biblioteca para el modelo de objetos
- Reproductor de Windows Media Mobile,library para el modelo de objetos
- Reproductor de Windows Media biblioteca, acerca de
- Reproductor de Windows Media biblioteca, servicios
- library,services
- library,about
- versiones de Reproductor de Windows Media,servicios de biblioteca
- enumeraciones, servicios de biblioteca
- events,library services
- samples,library services
- interfaces,servicios de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc6f073fa4c361f114589e080145a3cb3bb0a8c78736ba2dd1464332a7f7adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004524"
---
# <a name="about-library-services"></a>Acerca de Los servicios de biblioteca

En versiones anteriores de Reproductor de Windows Media, el software usaba una base de datos de biblioteca única para cada usuario. Esta base de datos se almacenaba en el equipo del usuario y estaba vinculada conceptualmente al usuario y a una instancia determinada del reproductor.

Reproductor de Windows Media 11 presenta los conceptos de varias bibliotecas remotas. Ahora, además de su biblioteca predeterminada o *local,* Reproductor de Windows Media puede mostrar el contenido recuperado de las bibliotecas de otros equipos conectados a una red, lo que podría incluir otros usuarios que hayan iniciado sesión en el mismo equipo. El reproductor también puede mostrar vistas de biblioteca de otros orígenes, como dispositivos habilitados para MTP o CDs de datos. Desde la perspectiva del usuario final, esto significa que el contenido multimedia digital ubicado en muchos lugares diferentes se puede administrar desde varias ubicaciones mediante la misma interfaz de usuario Reproductor de Windows Media usuario. Desde la perspectiva del desarrollador, esto significa que puede usar las interfaces COM del SDK de Reproductor de Windows Media para enumerar las bibliotecas disponibles y, a continuación, usarlas como ha usado la biblioteca local en versiones anteriores.

Para enumerar las bibliotecas disponibles, use la **interfaz IWMPLibraryServices.** Esta interfaz expone el [método IWMPLibraryServices::getCountByType,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) que recupera el recuento de bibliotecas de un tipo determinado. Los tipos de biblioteca se definen mediante la [enumeración WMPLibraryType.](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) Esta enumeración incluye un valor para la biblioteca local, wmpltLocal. Esto se debe a que la característica de servicios de biblioteca siempre permite trabajar con la biblioteca local mediante **IWMPLibraryServices** y las interfaces relacionadas.

> [!Note]  
> La **enumeración WMPLibraryType** incluye el valor wmpltRemote, que representa las bibliotecas multimedia compartidas por la red. Para acceder a esas bibliotecas compartidas, el control Player debe ejecutarse en modo remoto. Para obtener información sobre cómo ejecutar el control Player en modo remoto, vea [Remoting the Reproductor de Windows Media Control](remoting-the-windows-media-player-control.md).

 

Después de recuperar el recuento de bibliotecas, puede iterar la colección de bibliotecas disponibles llamando repetidamente a [IWMPLibraryServices::getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) en un bucle, pasando un nuevo valor de índice con cada iteración. Este método recupera un puntero a una [interfaz IWMPLibrary,](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) que representa la biblioteca individual.

Después de recuperar un puntero a **IWMPLibrary,** puede llamar a [IWMPLibrary::get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) para recuperar un puntero a una **interfaz IWMPMediaCollection.** Con este puntero de interfaz, puede trabajar con una biblioteca individual de forma muy parecido a como usaría la biblioteca local. También puede recuperar una cadena que contiene el nombre de la biblioteca llamando a [IWMPLibrary::get \_ name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), lo que resulta útil si necesita mostrar el nombre de la biblioteca al usuario. Puede llamar al [tipo IWMPLibrary::get \_](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) para obtener **el WMPLibraryType** de una biblioteca determinada.

Puede controlar el evento [IWMPEvents3::LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) para saber cuándo está disponible una biblioteca y el evento [IWMPEvents3::LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) para saber cuándo se desconecta una biblioteca. Cada uno de estos eventos proporciona un **puntero IWMPLibrary** que representa la biblioteca que se ha conectado o desconectado. Puede llamar a [IWMPLibrary::isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) para determinar si la biblioteca que se ha conectado o desconectado es una biblioteca que está usando actualmente.

Hay algunas diferencias importantes al trabajar con una biblioteca recuperada a través de la interfaz **IWMPLibraryServices** en comparación con trabajar con una biblioteca recuperada mediante [IWMPCore::get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection). Se aplican las diferencias siguientes:

-   Normalmente, puede recuperar los resultados de la consulta mucho más rápido de las bibliotecas recuperadas a través **de IWMPLibraryServices**. (Esto supone que otros factores, como los tiempos de acceso a la red y al disco duro, son iguales).
-   La lista de atributos de metadatos de elementos multimedia disponibles en las bibliotecas recuperadas a través de **IWMPLibraryServices** suele ser un subconjunto de los disponibles en la biblioteca local recuperada a través de [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore).
-   Si recupera la biblioteca local a través de **IWMPLibraryServices**, todos los mismos atributos están disponibles para su uso que los disponibles al recuperar la biblioteca local a través de **IWMPCore**. Sin embargo, podrá recuperar los resultados de la consulta mucho más rápido para los atributos que se usan con más frecuencia.
-   Debe usar colecciones de cadenas para crear elementos de interfaz de usuario cuando trabaje con bibliotecas recuperadas a través **de IWMPLibraryServices**. Por ejemplo, [IWMPMediaCollection2::getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) permite usar una consulta personalizada (representada por la interfaz **IWMPQuery)** para recuperar una colección de cadenas.
-   Es posible que las bibliotecas remotas recuperadas a través de la interfaz **IWMPLibraryServices** no siempre estén conectadas a la instancia de Player actual. Esto significa que es importante controlar los eventos **LibraryConnect** y **LibraryDisconnect** para saber cuándo cambia la disponibilidad de la biblioteca y controlar el evento [IWMPEvents3::StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) para saber cuándo se agregan o quitan cadenas de las colecciones de cadenas que se usan para mostrar los elementos de la interfaz de usuario. También debe controlar los **eventos StringCollectionChange** de la biblioteca local por motivos similares.

Es importante comprender que las colecciones de cadenas de una biblioteca determinada pueden cambiar en cualquier momento. Una colección de cadenas podría estar vacía al recuperarla por primera vez, como en el caso de una biblioteca que se ha conectado recientemente, pero el reproductor aún no ha enumerado su contenido. Por el contrario, es posible que una colección de cadenas ya contenga toda la información que necesita. En este caso, es posible que nunca reciba un evento **StringCollectionChange** porque el contenido de la biblioteca se había enumerado completamente antes de crear la consulta y no cambia nada más.

Por lo tanto, para mantener actualizada la interfaz de usuario, debe enumerar el contenido de la colección de cadenas al recuperar la interfaz **IWMPStringCollection** y controlar el evento **StringCollectionChange** para conocer las actualizaciones cuando se produce.

## <a name="sample"></a>Muestra

En el ejemplo denominado WMPML se muestra cómo trabajar con servicios de biblioteca. Para obtener más información sobre los Reproductor de Windows Media SDK, consulte [Ejemplos.](samples.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la biblioteca**](about-the-library.md)
</dt> <dt>

[**Acerca del objeto de consulta**](about-the-query-object.md)
</dt> <dt>

[**IWMPEvents3 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPLibrary (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**IWMPLibraryServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPQuery (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




