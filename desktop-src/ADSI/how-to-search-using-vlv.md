---
title: Cómo buscar mediante VLV
description: Active Directory admite búsquedas en la vista de lista virtual (VLV). Este estilo de búsqueda se ha diseñado específicamente para grandes conjuntos de resultados y permite que una aplicación muestre un subconjunto de miles de entradas sin tener que recuperar realmente cada entrada.
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- Cómo buscar mediante VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a24250c8e54ccb7917f86b193152c62810b93
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995633"
---
# <a name="how-to-search-using-vlv"></a>Cómo buscar mediante VLV

Active Directory admite búsquedas en la vista de lista virtual (VLV). Este estilo de búsqueda se ha diseñado específicamente para grandes conjuntos de resultados y permite que una aplicación muestre un subconjunto de miles de entradas sin tener que recuperar realmente cada entrada.

Hay dos maneras distintas de utilizar una búsqueda VLV. La primera consiste en recuperar los atributos de determinadas entradas en función de un desplazamiento numérico. Este método es útil cuando se recuperan los resultados de la búsqueda en respuesta a una operación de desplazamiento.

La segunda manera de usar las búsquedas VLV es buscar una parte o todo un atributo textual y mostrar solo los resultados de la búsqueda. Un ejemplo de uso de esto es una libreta de direcciones. Si el usuario escribe una "s", la aplicación puede usar una búsqueda VLV para buscar entradas con un nombre común que comience por "s". Si el usuario agrega una "m" a la "s", la aplicación puede usar otra búsqueda VLV para buscar entradas que tengan un nombre común que comience por "SM".

Para realizar una búsqueda VLV, indique a ADSI que use el control VLV. Para ello, llame al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) con una opción de búsqueda **\_ SEARCHPREF \_ VLV de ADS** con un valor **específico de ADSTYPE \_ Prov \_** . El **valor \_ \_ específico de ADSTYPE Prov** es un puntero a una estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) que contiene datos sobre la búsqueda. La función de ejemplo [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) muestra cómo establecer ambas preferencias de búsqueda.

Todas las búsquedas VLV deben usar la ordenación de resultados del servidor, que se lleva a cabo estableciendo el **\_ orden de los anuncios SEARCHPREF \_ \_ en** la preferencia de búsqueda. Para obtener más información sobre **el \_ \_ orden de \_ las preferencias de búsqueda de ADS SEARCHPREF** , vea [ordenar los resultados de la búsqueda con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).

Cuando se realiza una búsqueda VLV, se devuelve una determinada cantidad de metadatos sobre la búsqueda en una columna que se recupera llamando a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con el identificador de **\_ \_ respuesta VLV de ADS** . Estos datos se encuentran en una estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Los miembros **dwContentCount** y **lpContextID** son de especial importancia. El miembro **dwContentCount** contendrá el número de resultados que cumplen los criterios de búsqueda VLV. Este valor se puede usar como una estimación del número total de elementos que se devolverían para una búsqueda de ese tipo. El miembro **lpContextID** contiene un valor definido por el servidor que se puede pasar a la siguiente búsqueda para identificar la búsqueda. El uso de **lpContextID** puede mejorar el rendimiento de la búsqueda. Tenga en cuenta que **lpContextID** es un valor definido por el servidor y su longitud está contenida en el miembro **dwContextIDLength** . Este búfer se libera cuando se llama al método [**IDirectorySearch:: FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) , por lo que el llamador debe asignar un búfer del tamaño adecuado y copiar y guardar el contenido del búfer entre las búsquedas.

Para obtener más información sobre el control VLV de LDAP, vea [Buscar con el control VLV de LDAP](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control).

Para más información, consulte:

-   Obtener el número de elementos
-   Buscar por desplazamiento
-   Buscar por cadena
-   [Código de ejemplo para usar una búsqueda VLV](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>Obtener el número de elementos

**Para obtener una estimación del número de elementos que se devolverán para una búsqueda determinada, realice los pasos siguientes.**

1.  Rellene una estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con todos los valores cero o **null** .
2.  Rellene [**una \_ \_ información de ADS SEARCHPREF**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) con los siguientes valores.

    -   Establezca el miembro **dwSearchPref** en **ADS \_ SEARCHPREF \_ VLV**.
    -   Establezca el miembro **vValue. dwType** en **ADSTYPE \_ Prov \_ específico**.
    -   Establezca el miembro **vValue. ProviderSpecific. dwLength** en el tamaño de la [**estructura \_ VLV de ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
    -   Establezca el miembro **vValue. ProviderSpecific. lpValue** en la dirección de la estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) del paso 1.

3.  Rellene una estructura [**\_ SORTKEY de ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) tal y como se muestra en [ordenar los resultados de la búsqueda con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md) para ordenar por el atributo deseado.
4.  Rellene [**otra \_ \_ información de ADS SEARCHPREF**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) para agregar la estructura de la clasificación de [**anuncios \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) a las preferencias de búsqueda como se muestra en [ordenar los resultados de la búsqueda con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).
5.  Agregue las demás preferencias de búsqueda que desee y llame a [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) para establecer las preferencias de búsqueda.
6.  Realice la búsqueda con [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
7.  Obtenga la primera fila de resultados mediante una llamada a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
8.  Llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con la **\_ \_ respuesta VLV de ADS** para obtener los metadatos de búsqueda VLV.
9.  Convierta el **pADsValues->ProviderSpecific. lpValue** de la estructura de la [**columna de \_ búsqueda \_ de ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntero de estructura [**\_ VLV de ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . El miembro **dwContentCount** de esta **estructura \_ VLV de ADS** contiene el número aproximado de elementos que se devolverían mediante una búsqueda de ese tipo.
10. Si se van a realizar otras búsquedas VLV del mismo tipo, realice una copia de los datos de **lpContextID** y preserve la siguiente búsqueda de VLV.

La función de ejemplo [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) muestra cómo hacerlo.

## <a name="searching-by-offset"></a>Buscar por desplazamiento

Una cosa que hace que las búsquedas VLV sean tan rápidas es que es posible buscar un resultado específico mediante un desplazamiento numérico. Por ejemplo, si una búsqueda da como resultado la devolución de 10.000 elementos, una búsqueda VLV permite obtener la información de aproximadamente el elemento 4072nd sin tener que recuperar todos los elementos antes del elemento en cuestión.

Los desplazamientos se especifican como una relación entre el desplazamiento y el recuento de contenido. Las proporciones son útiles porque es posible que el servidor no tenga una estimación precisa del número de entradas que hay en la lista o puede que el tamaño de la lista cambie durante el tiempo que el usuario está explorando. Dado que debe indicar el principio y el final de la lista, puede usar un valor estimado para el recuento de contenido en la primera solicitud de búsqueda, junto con un valor de desplazamiento. El servidor usa estos datos para calcular los desplazamientos correspondientes dentro de la lista, en función de su idea del recuento de contenido, que se envía en su respuesta al cliente a través del miembro **dwContentCount** de la estructura [**\_ VLV de ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Por ejemplo, si calcula que el tamaño de la lista es 3000 y desea que el desplazamiento sea la entrada de lista 1500, debe establecer **dwContentCount** en 3000 y **dwOffset** en 1500. Si el servidor calcula que el tamaño de la lista real es 4500, volverá a calcular el desplazamiento a 2250 y devolverá las nuevas estimaciones en **dwContentCount** y **dwOffset**.

> [!Note]
>
> Todos los valores numéricos en una búsqueda VLV son aproximaciones y no se deben usar para los valores absolutos. Por ejemplo, si emite una búsqueda VLV para el elemento 50 en una ración de 100, no se garantiza que obtenga el elemento central exacto.
>
> **Para buscar un elemento determinado por desplazamiento, realice los pasos siguientes.**
>
> 1.  Rellene una estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con los valores siguientes. Los miembros adicionales de la estructura se deben establecer en cero o **null**.
>
>     -   Establezca el miembro **dwContentCount** en el valor máximo de la relación de los elementos que se van a recuperar.
>     -   Establezca el miembro **dwOffset** en la relación, relativa a **dwContentCount**, del elemento o de los elementos que se van a recuperar.
>     -   Establezca el miembro **lpContextID** en la dirección de la copia del búfer de ID. de contexto y **dwContextIDLength** en la longitud, en bytes, del búfer de ID. de contexto. Si no se ha guardado ningún ID. de contexto, ambos miembros deben ser cero o **null**.
>
> 2.  Establezca las preferencias de búsqueda como se muestra en los pasos 2 a 5 del procedimiento obtener el número de elementos.
> 3.  Realice la búsqueda con [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
> 4.  Obtenga la primera fila de resultados mediante una llamada a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
> 5.  Llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con el nombre del atributo que se va a recuperar para obtener los datos reales del elemento solicitado.
> 6.  Llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con la **\_ \_ respuesta VLV de ADS** para obtener los metadatos de búsqueda VLV.
> 7.  Convierta el **pADsValues->ProviderSpecific. lpValue** de la estructura de la [**columna de \_ búsqueda \_ de ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntero de estructura [**\_ VLV de ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
> 8.  Realice una copia de los datos de **lpContextID** y preserve la siguiente búsqueda de VLV.

 

La función de ejemplo [**GetVLVItemText**](example-code-for-using-a-vlv-search.md) muestra cómo hacerlo.

También es posible recuperar más de una fila de datos con una sola llamada de búsqueda. Esto se hace en el paso 1 estableciendo los miembros **dwBeforeCount** y **dwAfterCount** de la estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) adecuadamente. El miembro **dwBeforeCount** contiene el número de elementos que aparecen en la lista antes del elemento en cuestión y el miembro **dwAfterCount** contiene el número de elementos que aparecen en la lista después del elemento en cuestión. Ambos recuentos excluyen el propio elemento, por lo que si se establece **dwBeforeCount** en 10 y **dwAfterCount** en 10, se devolverá un total de 21 elementos. Esta opción habilita el almacenamiento en caché de los resultados de la búsqueda en el lado cliente.

## <a name="searching-by-string"></a>Buscar por cadena

También es posible usar una búsqueda VLV para buscar elementos que tengan un atributo de cadena cuyo valor coincida con la totalidad o una parte de una cadena sin tener que recuperar todos los elementos. La coincidencia de cadenas se realiza con el atributo especificado en la estructura de los [**anuncios \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) de clasificación de la preferencia de búsqueda **\_ \_ ordenar \_ por SEARCHPREF de anuncios** .

**Para buscar un elemento determinado por cadena, realice los pasos siguientes.**

1.  Rellene una estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con los valores siguientes. Los miembros adicionales de la estructura se deben establecer en cero o **null**.

    -   Establezca el miembro **pszTarget** en un puntero a una cadena terminada en null que contenga la cadena que se va a buscar.
    -   Establezca el miembro **lpContextID** en la dirección de la copia del búfer de ID. de contexto y **dwContextIDLength** en la longitud, en bytes, del búfer de ID. de contexto. Si no se ha guardado ningún ID. de contexto, ambos miembros deben ser cero o **null**.

2.  Establezca las preferencias de búsqueda como se muestra en los pasos 2 a 5 del procedimiento obtener el número de elementos.
3.  Realice la búsqueda con [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
4.  Obtenga la primera fila de resultados mediante una llamada a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
5.  Llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con el nombre del atributo que se va a recuperar para obtener los datos reales del elemento solicitado.
6.  Llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con la **\_ \_ respuesta VLV de ADS** para obtener los metadatos de búsqueda VLV.
7.  Convierta el **pADsValues->ProviderSpecific. lpValue** de la estructura de la [**columna de \_ búsqueda \_ de ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntero de estructura [**\_ VLV de ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
8.  Realice una copia de los datos de **lpContextID** y preserve la siguiente búsqueda de VLV. Si es necesario, el miembro **dwOffset** contiene el índice basado en uno del primer elemento cuyo atributo de cadena comienza con el valor especificado en **pszTarget**.

La función de ejemplo [**GetVLVItemsByString**](example-code-for-using-a-vlv-search.md) muestra cómo hacerlo.

De forma similar a la búsqueda por índice, también es posible recuperar más de una fila de datos con una sola llamada de búsqueda. Esto se logra de la misma manera estableciendo los miembros **dwBeforeCount** y **dwAfterCount** de la estructura de [**ADS \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) adecuadamente.

 

 