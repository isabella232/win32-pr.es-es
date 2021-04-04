---
title: Llamar a WDS mediante programación
description: La búsqueda en el escritorio de Microsoft Windows (WDS) 2. x se puede consultar mediante programación con los métodos ExecuteQuery y ExecuteSQLQuery de la interfaz ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791439"
---
# <a name="calling-wds-programmatically"></a>Llamar a WDS mediante programación

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

La búsqueda en el escritorio de Microsoft Windows (WDS) 2. x se puede consultar mediante programación con los métodos **ExecuteQuery** y **ExecuteSQLQuery** de la interfaz [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) . El método **ExecuteQuery** devuelve un conjunto de registros del índice basándose en el texto de la consulta, las columnas y las restricciones que se pasan como parámetros. El método **ExecuteSQLQuery** también devuelve un conjunto de registros de resultados, pero requiere que se pase el comando exacto lenguaje de consulta estructurado (SQL). La mayoría de los escenarios deben usar **ExecuteQuery** .

## <a name="regular-queries"></a>Consultas regulares

Las consultas normales se escriben en el cuadro de entrada de WDS por parte del usuario, incluida la [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md). La consulta se pasa a **ExecuteQuery** junto con las columnas de [esquema](-search-2x-wds-schematable.md) de WDS 2. x que se van a devolver, la columna y el orden en que se ordenarán los resultados y las cláusulas para restringir los resultados.

El método tiene el formato:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Dirección | Variable           | Descripción                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En        | lpcwstrQuery       | El texto de la consulta. Esta consulta es la misma que una consulta escrita en el cuadro de texto Buscar en la interfaz de usuario de búsqueda en el escritorio de Windows. <br/> Por ejemplo: `"from:Zara dinner plans"`<br/> |
| En        | lpcwstrColumn      | Columnas que se van a incluir, separadas por comas. <br/> Por ejemplo: `"DocTitle, Url"`<br/>                                                                                            |
| En        | lpcwstrSort        | Columna de invalidación por la que se va a ordenar seguido de ASC para ascendente o DESC en orden descendente. <br/> Por ejemplo: `"LastAuthor DESC"`<br/>                                                  |
| En        | lpcwstrRestriction | Restricciones para anexar a través de las cláusulas WHERE en la búsqueda de escritorio de Windows seleccione. <br/> Por ejemplo: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| Fuera       | ppiRs              | El conjunto de registros resultante<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Consultas SQL

El método **ISearchDesktop.ExecuteSQLQuery** se usa para enviar consultas directas de la base de datos WDS. La sintaxis de las consultas es similar a la que se usa para SharePoint Server, junto con la capacidad de usar cláusulas SQL GROUP BY de estilo monarca. La consulta se ejecuta en el índice exactamente como se pasa sin ningún procesamiento adicional de la sintaxis de consulta avanzada a medida que lo hace la API ExecuteQuery.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

El método tiene el formato:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Dirección | Variable   | Descripción                                    |
|-----------|------------|------------------------------------------------|
| En        | lpcwstrSQL | Consulta SQL que se va a ejecutar en el índice de WDS |
| Fuera       | ppiRs      | El conjunto de registros resultante                       |



 

Recursos:

-   Archivos de compatibilidad para la interfaz ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip
-   Ejemplo de C# de ISearchDesktop: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Código de C++ de ejemplo

> [!Note]
>
> ESTE CÓDIGO E INFORMACIÓN SE PROPORCIONA "TAL CUAL" SIN GARANTÍA DE NINGÚN TIPO, YA SEA EXPRESA O IMPLÍCITA, INCLUIDAS, ENTRE OTRAS, LAS GARANTÍAS IMPLÍCITAS DE COMERCIABILIDAD O IDONEIDAD PARA UN PROPÓSITO DETERMINADO.
>
> Copyright (C) Microsoft. Todos los derechos reservados.

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Llamar a WDS desde páginas web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

