---
title: Llamar a WDS mediante programación
description: Microsoft Windows Desktop Search (WDS) 2.x se puede consultar mediante programación mediante los métodos ExecuteQuery y ExecuteSQLQuery en la interfaz ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359064"
---
# <a name="calling-wds-programmatically"></a>Llamar a WDS mediante programación

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Microsoft Windows Desktop Search (WDS) 2.x se puede consultar mediante programación mediante los métodos **ExecuteQuery** y **ExecuteSQLQuery** en la interfaz [**ISearchDesktop.**](/previous-versions//aa965729(v=vs.85)) El **método ExecuteQuery** devuelve un conjunto de registros del índice en función del texto de la consulta, las columnas y las restricciones que se pasan como parámetros. El **método ExecuteSQLQuery** también devuelve un conjunto de registros de resultados, pero requiere que se pase el comando Lenguaje de consulta estructurado (SQL) exacto. **ExecuteQuery** debe usarse en la mayoría de los escenarios.

## <a name="regular-queries"></a>Consultas normales

Las consultas normales son las que el usuario escribe en el cuadro de entrada de WDS, incluida toda la [sintaxis de consulta avanzada.](-search-2x-wds-aqsreference.md) La consulta se pasa a **ExecuteQuery** junto con las columnas de esquema wds 2.x [](-search-2x-wds-schematable.md) que se devuelven, la columna y el orden para ordenar los resultados y cualquier cláusula por la que restringir los resultados.

El método tiene el formato:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Dirección | Variable           | Descripción                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En        | lpcwstrQuery       | El texto de la consulta. Esta consulta es la misma que una consulta que se escribe en el cuadro de texto de búsqueda de la Windows de usuario de Búsqueda de escritorio. <br/> Por ejemplo: `"from:Zara dinner plans"`<br/> |
| En        | lpcwstrColumn      | Columnas que se incluirán, separadas por comas. <br/> Por ejemplo: `"DocTitle, Url"`<br/>                                                                                            |
| En        | lpcwstrSort        | Columna de invalidación por la que se va a ordenar seguido de ASC para ascendente o DESC para descendente. <br/> Por ejemplo: `"LastAuthor DESC"`<br/>                                                  |
| En        | lpcwstrRestriction | Restricciones para anexar a través de cláusulas WHERE en la Windows búsqueda de escritorio. <br/> Por ejemplo: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| Fuera       | pppRs              | Conjunto de registros resultante<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Consultas SQL

El **método ISearchDesktop.ExecuteSQLQuery** se usa para enviar consultas de base de datos WDS directas. La sintaxis de las consultas es similar a la que se usa para SharePoint Server, junto con la capacidad de usar cláusulas group by de estilo SQL estilo de la conducción. La consulta se ejecuta en el índice exactamente como se pasa sin ningún procesamiento adicional de la sintaxis de consulta avanzada como hace la API ExecuteQuery.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

El método tiene el formato:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Dirección | Variable   | Descripción                                    |
|-----------|------------|------------------------------------------------|
| En        | lpcwstrSQL | Consulta SQL que se ejecutará en el índice wds |
| Fuera       | pppRs      | Conjunto de registros resultante                       |



 

Recursos:

-   Archivos de compatibilidad para la interfaz ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip
-   Ejemplo de C# de ISearchDesktop: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Código de C++ de ejemplo

> [!Note]
>
> ESTE CÓDIGO E INFORMACIÓN SE PROPORCIONAN "TAL Y COMO ESTÁN" SIN GARANTÍA DE NINGÚN TIPO, YA SEA EXPRESA O IMPLÍCITA, INCLUIDAS, ENTRE OTRAS, LAS GARANTÍAS IMPLÍCITAS DE COMERCIABILIDAD O IDONEIDAD PARA UN PROPÓSITO DETERMINADO.
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

[Llamada a WDS desde Páginas web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

