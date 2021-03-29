---
title: Buscar con la interfaz IDirectorySearch
description: La interfaz IDirectorySearch proporciona una interfaz de alto nivel y poca sobrecarga para consultar datos de un directorio o un catálogo global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Buscar con la interfaz IDirectorySearch ADSI
- Consultas ADSI, interfaces de consulta, IDirectorySearch
- ADSI ADSI, código de ejemplo C/C++, buscar un directorio con IDirectorySearch
- ADSI de IDirectorySearch, usar para buscar en un directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904829"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Buscar con la interfaz IDirectorySearch

La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona una interfaz de alto nivel y poca sobrecarga para consultar datos de un directorio o un catálogo global. La interfaz com **IDirectorySearch** solo se puede usar con vtable y, por lo tanto, no está disponible para los entornos de desarrollo basados en automatización.

**Para realizar una búsqueda**

1.  Enlazar a un objeto en el directorio.
2.  Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener el puntero [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .
3.  Ejecute la búsqueda con el puntero [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Llame al método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) y pase un filtro de búsqueda, los nombres de atributo solicitados y otros parámetros.

Para obtener más información sobre la sintaxis del filtro de búsqueda, consulte [Sintaxis de filtro de búsqueda](search-filter-syntax.md).

La ejecución de la consulta es específica del proveedor. Con algunos proveedores, la ejecución de la consulta real no se realiza hasta que se llama a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) . La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funciona directamente con los filtros de búsqueda. No se requieren el dialecto SQL ni el dialecto LDAP.

La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) proporciona métodos para enumerar el conjunto de resultados, fila por fila. El método [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera la primera fila y [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) le lleva a la fila siguiente de la fila actual. Cuando se ha alcanzado la última fila, al llamar a estos métodos, se devuelve el \_ \_ código de error de filas nomores \_ . Por el contrario, [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) mueve una fila cada vez. Un \_ \_ \_ valor devuelto por un número de filas de los anuncios de S indica que ha alcanzado la primera fila del conjunto de resultados. Estos métodos operan en el conjunto de resultados, residente en memoria, en el cliente. Por lo tanto, cuando se realizan búsquedas en páginas y asincrónicas y la \_ opción resultados de caché está desactivada \_ , el desplazamiento hacia atrás puede tener consecuencias inesperadas.

Cuando haya encontrado la fila adecuada, llame a [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para obtener elementos de datos, columna por columna. Para cada llamada, se pasa el nombre de la columna de interés. El elemento de datos devuelto es un puntero a una estructura de [**\_ \_ columnas de búsqueda de ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) . **Getcolumn (** asigna esta estructura automáticamente, pero debe liberarla con [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Llame a [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) para completar la operación de búsqueda.

**Para realizar una búsqueda de directorio**

1.  Enlazar a un proveedor LDAP. Puede ser un controlador de dominio o un proveedor de catálogo global.
2.  Recuperar la interfaz com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) con una llamada a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); es posible que esta operación se haya realizado en el paso 1 durante el enlace inicial.

    Opcionalmente, llame a [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) para seleccionar las opciones para administrar los resultados de la búsqueda.

3.  Llame a [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch). En función de las opciones establecidas en [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , puede iniciar la ejecución de la consulta.
4.  Llame a [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para trasladar el índice de fila (interno a [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) a la primera fila.
5.  Lea los datos de la fila mediante [**getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)y, a continuación, llame a [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) para liberar la memoria asignada por **getcolumn (**.
6.  Repita el paso 5 hasta que se recuperen todos los datos del resultado de la búsqueda, o hasta que [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) devuelva el resto de filas de S \_ \_ \_ .
7.  Llame a [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) y [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) cuando haya finalizado.

En el ejemplo de código siguiente se muestra este escenario. Para empezar a enlazar a ADSI, llame a la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


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



Esto proporciona un puntero a la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

Ahora que hay una interfaz COM para una instancia de IDirectoryInterface, llame a [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Cree una matriz de nombres de atributo para preparar la llamada a la función [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . Los nombres de atributo se definen en el esquema de Active Directory. Para obtener más información acerca de la definición de esquema, vea [modelo de esquema ADSI](adsi-schema-model.md). Se devuelven los nombres de atributo enumerados, si el objeto lo admite, como el conjunto de resultados de la búsqueda.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Ahora, llame a la función [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . La búsqueda no se ejecuta hasta que se llama al método [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Llame a [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para iterar las filas en el resultado. A continuación, se consulta a cada fila el atributo "Description". Si se encuentra el atributo, se muestra.


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



Para finalizar la búsqueda, llame al método [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .

Tenga en cuenta que si no se establece un tamaño de página, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) se bloquea hasta que se devuelve el conjunto de resultados completo al cliente. Si se establece tamaño de página, **GetNextRow** se bloquea hasta que se devuelve la primera página (tamaño de página = número de filas de una página). Si se establece el tamaño de página y la consulta se va a ordenar y no está buscando por lo menos un atributo indexado, se omite el valor de tamaño de página y el servidor calcula el conjunto de resultados completo antes de devolver los datos. Esto tiene el efecto de que el **GetNextRow** se bloquee hasta que se complete la consulta.

> [!Note]  
> Para cambiar esta consulta de una búsqueda de directorio a una búsqueda de catálogo global, se cambia la llamada a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 