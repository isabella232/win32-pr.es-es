---
title: Paginación con IDirectorySearch
description: La paginación especifica cuántas filas devuelve el servidor al cliente.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paginación con IDirectorySearch ADSI
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Paginación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48494c01831e6b69931fc6b6f779ed9b042b7fecaaf17fa62286c094a926ba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838945"
---
# <a name="paging-with-idirectorysearch"></a>Paginación con IDirectorySearch

La paginación especifica cuántas filas devuelve el servidor al cliente. Una página se puede definir por el número de filas o un límite de tiempo. El objeto COM ADSI recupera cada página de resultados en función de los valores enumerados en la tabla siguiente. El autor de la llamada llama a [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) cuando ha llegado al final de la página y el objeto COM ADSI recupera la página siguiente.



| Valor                                   | Descripción                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ SEARCHPREF \_ PAGESIZE**           | Especifica el número máximo de filas que se devolverán en una página.                                                                                                                                                                                            |
| **LÍMITE \_ DE TIEMPO PAGINADO DE SEARCHPREF \_ \_ DE \_ ADS** | Especifica el tiempo máximo, en segundos, que el servidor debe dedicar a recopilar una página de resultados antes de devolver la página al cliente. Si se alcanza el límite, el servidor detiene la búsqueda y devuelve las filas ya recuperadas para la página. |



 

Si no se establece ninguna de estas preferencias de búsqueda, el valor predeterminado no es ninguna paginación. Las búsquedas de Active Directory realizadas sin paginación se limitan a devolver un máximo de los 1000 primeros registros, por lo que debe usar una búsqueda paginada si existe la posibilidad de que el conjunto de resultados contenga más de 1000 elementos.

Una operación de búsqueda puede dar lugar a la devolución de un gran número de objetos. Si el servidor devuelve el resultado en un conjunto, podría reducir el rendimiento del cliente y el servidor, así como afectar a la carga de red. Las búsquedas paginadas se pueden usar para evitarlo. En una búsqueda paginada, el cliente puede aceptar resultados en paquetes más pequeños. El tamaño de un paquete se conoce como tamaño de página de búsqueda.

Las búsquedas paginadas ofrecen ventajas tanto para el cliente como para el servidor. El cliente puede tener más capacidad de respuesta para presentar los resultados a los usuarios. Esto es especialmente relevante para las herramientas gráficas de interfaz de usuario que pueden comenzar el proceso de visualización de la ventana mientras el otro subproceso recibe simultáneamente los datos.

En el lado servidor, las búsquedas paginadas hacen que la operación sea escalable. Por ejemplo, si cien clientes emiten solicitudes de búsqueda simultáneamente y, de media, cada cliente recibe dos cientos de objetos. Si no se especifica ningún tamaño de página, en el peor de los casos, el servidor debe tener memoria suficiente para contener 20 000 objetos. Por el contrario, si cada cliente especifica un tamaño de página para ser, por ejemplo, diez objetos, el requisito de memoria en el servidor se reduce en un factor de 20.

Además, mediante una búsqueda paginada, un cliente puede abandonar la operación en curso. En cambio, en una búsqueda no paginada, el cliente recibe un conjunto de resultados en un paquete. Esto puede reducir el rendimiento de la red.

ADSI controla el tamaño de página del cliente. El cliente no tiene que contar el número de objetos en curso. ADSI encapsula la interacción del servidor para el cliente. Desde la perspectiva del cliente, la búsqueda devuelve un conjunto de resultados completo.

Se recomienda usar la paginación.

Para especificar un tamaño máximo de página, establezca una opción de búsqueda **ADS \_ SEARCHPREF \_ PAGESIZE** con un valor **DE \_ ADSTYPE INTEGER** establecido en el número máximo de filas por página de la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS que se pasa al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

En el ejemplo de código siguiente se muestra cómo establecer el tamaño máximo de página.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Para especificar un tiempo de página, establezca una opción de búsqueda **ADS \_ SEARCHPREF \_ PAGED \_ TIME \_ LIMIT** con un valor **DE ADSTYPE \_ INTEGER** establecido en el número máximo de segundos que el servidor debe dedicar a recuperar una página de la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

En el ejemplo de código siguiente se muestra cómo especificar el tiempo de página.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




