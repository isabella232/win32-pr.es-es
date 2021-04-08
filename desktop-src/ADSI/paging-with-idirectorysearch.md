---
title: Paginación con IDirectorySearch
description: La paginación especifica el número de filas que devuelve el servidor al cliente.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paginación con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, paginación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993848"
---
# <a name="paging-with-idirectorysearch"></a>Paginación con IDirectorySearch

La paginación especifica el número de filas que devuelve el servidor al cliente. Una página puede definirse por el número de filas o un límite de tiempo. El objeto COM ADSI recupera cada página de resultados basándose en los valores que se muestran en la tabla siguiente. El llamador llama a [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) cuando ha alcanzado el final de la página y el objeto com ADSI recupera la página siguiente.



| Value                                   | Descripción                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_paginación de ADS SEARCHPREF \_**           | Especifica el número máximo de filas que se van a devolver en una página.                                                                                                                                                                                            |
| **\_límite de \_ tiempo paginado de SEARCHPREF ADS \_ \_** | Especifica el tiempo máximo, en segundos, que el servidor debe gastar en recopilar una página de resultados antes de devolver la página al cliente. Si se alcanza el límite, el servidor detiene la búsqueda y devuelve las filas ya recuperadas para la página. |



 

Si no se establece ninguna de estas preferencias de búsqueda, el valor predeterminado es sin paginación. Las búsquedas de Active Directory realizadas sin paginación se limitan a devolver un máximo de los primeros 1000 registros, por lo que debe usar una búsqueda paginada si existe la posibilidad de que el conjunto de resultados contenga más de 1000 elementos.

Una operación de búsqueda puede dar lugar a que se devuelva un gran número de objetos. Si el servidor devuelve el resultado en un conjunto, podría reducir el rendimiento del cliente y del servidor, así como afectar a la carga de la red. Las búsquedas paginadas se pueden usar para evitar esto. En una búsqueda paginada, el cliente puede aceptar los paquetes más pequeños. El tamaño de un paquete se conoce como el tamaño de la página de búsqueda.

Las búsquedas paginadas ofrecen ventajas tanto para el cliente como para el servidor. El cliente puede tener mayor capacidad de respuesta en la presentación de los resultados a los usuarios. Esto es especialmente relevante para las herramientas de interfaz gráfica de usuario que pueden iniciar el proceso de visualización de la ventana mientras el otro subproceso recibe los datos simultáneamente.

En el lado del servidor, las búsquedas paginadas hacen que la operación sea escalable. Por ejemplo, si los clientes 100 emiten solicitudes de búsqueda simultáneamente y, en el promedio, cada cliente recibe 200 objetos. Si no se especifica ningún tamaño de página, en el peor de los casos, el servidor debe tener suficiente memoria para contener 20.000 objetos. Por el contrario, si cada cliente especifica un tamaño de página, por ejemplo, diez objetos, el requisito de memoria en el servidor se reduce por un factor de 20.

Además, mediante una búsqueda paginada, un cliente puede abandonar la operación en curso. Por el contrario, en una búsqueda no paginada, el cliente recibe un conjunto de resultados en un paquete. Esto puede reducir el rendimiento de la red.

ADSI controla el tamaño de página para el cliente. El cliente no tiene que contar el número de objetos en curso. ADSI encapsula la interacción del servidor para el cliente. Desde la perspectiva del cliente, la búsqueda devuelve un conjunto de resultados completo.

Se recomienda usar la paginación.

Para especificar un tamaño de página máximo, establezca la opción de búsqueda de **\_ \_ SEARCHPREF de anuncios de ADS** con un valor **\_ entero de ADSTYPE** establecido en el número máximo de filas por página de la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

En el ejemplo de código siguiente se muestra cómo establecer el tamaño máximo de página.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Para especificar un tiempo de página, establezca una opción de búsqueda de **\_ \_ \_ \_ límite de tiempo paginado de SEARCHPREF** con un valor **\_ entero de ADSTYPE** establecido en el número máximo de segundos que el servidor debe invertir en recuperar una página en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

En el ejemplo de código siguiente se muestra cómo especificar la hora de la página.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




