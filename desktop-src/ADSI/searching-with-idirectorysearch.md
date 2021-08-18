---
title: Búsqueda con la interfaz IDirectorySearch
description: La interfaz IDirectorySearch proporciona una interfaz de alto nivel y baja sobrecarga para consultar datos de un directorio o un catálogo global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Búsqueda con el ADSI de la interfaz IDirectorySearch
- Consultas ADSI, interfaces de consulta, IDirectorySearch
- ADSI ADSI, código de ejemplo C/C++, buscar un directorio con IDirectorySearch
- IDirectorySearch ADSI , Usar para buscar un directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46700c48f82955bd01967808cd30f2fa078e3b6c998fb3beaac4bf7c7fe8707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023224"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Búsqueda con la interfaz IDirectorySearch

La [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona una interfaz de alto nivel y baja sobrecarga para consultar datos de un directorio o un catálogo global. La interfaz COM **de IDirectorySearch** solo se puede usar con una vtable y, por tanto, no está disponible para entornos de desarrollo basados en Automation.

**Para realizar una búsqueda**

1.  Enlace a un objeto en el directorio .
2.  Llame [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener el [**puntero IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
3.  Ejecute la búsqueda mediante el [**puntero IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Llame al [**método IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) y pase un filtro de búsqueda, los nombres de atributo solicitados y otros parámetros.

Para obtener más información sobre la sintaxis de filtro de búsqueda, vea [Sintaxis de filtro de búsqueda.](search-filter-syntax.md)

La ejecución de consultas es específica del proveedor. Con algunos proveedores, la ejecución de la consulta real no se produce hasta que se llama a [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch::GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) La [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funciona directamente con filtros de búsqueda. No se SQL el dialecto ldap ni el dialecto LDAP.

La [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona métodos para enumerar el conjunto de resultados, fila por fila. El [**método IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera la primera fila e [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) le mueve a la siguiente fila de la fila actual. Cuando haya alcanzado la última fila, la llamada a estos métodos devuelve el código de error S \_ ADS \_ NOMORE \_ ROWS. Por el contrario, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) le mueve una fila a la vez. Un valor devuelto S ADS NOMORE ROWS indica \_ que ha alcanzado la primera fila del conjunto de \_ \_ resultados. Estos métodos funcionan en el conjunto de resultados, que residen en la memoria, en el cliente. Por lo tanto, cuando se realizan búsquedas paginadas y asincrónicas y la opción RESULTADOS DE CACHÉ está desactivada, el desplazamiento \_ hacia atrás puede tener \_ consecuencias inesperadas.

Cuando haya ubicado la fila adecuada, llame a [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para obtener elementos de datos, columna por columna. Para cada llamada, se pasa el nombre de la columna de interés. El elemento de datos devuelto es un puntero a una [**estructura \_ ADS SEARCH \_ COLUMN.**](/windows/desktop/api/Iads/ns-iads-ads_search_column) **GetColumn** le asigna esta estructura, pero debe liberarla mediante [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Llame [**a CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) para completar la operación de búsqueda.

**Para realizar una búsqueda de directorios**

1.  Enlace a un proveedor LDAP. Puede ser un controlador de dominio o un proveedor de catálogo global.
2.  Recupere la interfaz COM [**de IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) con una llamada a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Es posible que esta operación se haya realizado en el paso 1 durante el enlace inicial.

    Opcionalmente, llame a [**SetSearchPreference para**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) seleccionar opciones para controlar los resultados de la búsqueda.

3.  Llame [**a ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) Dependiendo de las opciones establecidas [**en SetSearchPreference,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) esto puede, o no, comenzar la ejecución de la consulta.
4.  Llame [**a GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para mover el índice de fila (interno a [**IDirectorySearch)**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)a la primera fila.
5.  Lea los datos de la fila mediante [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)y, a continuación, llame [**a FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) para liberar la memoria asignada por **GetColumn**.
6.  Repita el paso 5 hasta que se recuperen todos los datos del resultado de la búsqueda o hasta [**que GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) devuelva S \_ ADS \_ NOMORE \_ ROWS.
7.  Llame [**a AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) y [**CloseSearchHandle cuando**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) haya finalizado.

En el ejemplo de código siguiente se muestra este escenario. Para iniciar el enlace a ADSI, llame [**a la función ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



Esto proporciona un puntero a la [**interfaz IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Ahora que hay una interfaz COM para una instancia de IDirectoryInterface, llame a [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Compile una matriz de nombres de atributo para prepararse para llamar a la [**función IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) Los nombres de atributo se definen dentro del esquema de Active Directory. Para obtener más información sobre la definición de esquema, vea [AdsI Schema Model](adsi-schema-model.md). Los nombres de atributo enumerados se devuelven, si el objeto lo admite, como conjunto de resultados de la búsqueda.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Ahora, llame a la [**función ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) La búsqueda no se ejecuta hasta que se llama al [**método GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Llame [**a GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para iterar filas en el resultado. A continuación, se consulta cada fila para el atributo "description". Si se encuentra el atributo, se muestra.


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



Para finalizar la búsqueda, llame al [**método AbandonSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch)

Tenga en cuenta que si no se establece un tamaño de página, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) se bloquea hasta que se devuelve al cliente todo el conjunto de resultados. Si se establece el tamaño de página, **GetNextRow** se bloquea hasta que se devuelve la primera página (tamaño de página = número de filas de una página). Si se establece el tamaño de página y la consulta se va a ordenar y no se busca en al menos un atributo indexado, se omite el valor de tamaño de página y el servidor calcula todo el conjunto de resultados antes de devolver los datos. Esto tiene el efecto de bloqueo **GetNextRow** hasta que se completa la consulta.

> [!Note]  
> Para cambiar esta consulta de una búsqueda de directorio a una búsqueda de catálogo global, se cambia la llamada [**ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 