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
# <a name="calling-wds-programmatically"></a><span data-ttu-id="0e5d2-103">Llamar a WDS mediante programación</span><span class="sxs-lookup"><span data-stu-id="0e5d2-103">Calling WDS Programmatically</span></span>

> [!NOTE]
> <span data-ttu-id="0e5d2-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0e5d2-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="0e5d2-106">La búsqueda en el escritorio de Microsoft Windows (WDS) 2. x se puede consultar mediante programación con los métodos **ExecuteQuery** y **ExecuteSQLQuery** de la interfaz [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e5d2-106">Microsoft Windows Desktop Search (WDS) 2.x can be queried programmatically using the **ExecuteQuery** and **ExecuteSQLQuery** methods in the [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) interface.</span></span> <span data-ttu-id="0e5d2-107">El método **ExecuteQuery** devuelve un conjunto de registros del índice basándose en el texto de la consulta, las columnas y las restricciones que se pasan como parámetros.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-107">The **ExecuteQuery** method returns a record set from the index based on the query text, columns, and restrictions passed as parameters.</span></span> <span data-ttu-id="0e5d2-108">El método **ExecuteSQLQuery** también devuelve un conjunto de registros de resultados, pero requiere que se pase el comando exacto lenguaje de consulta estructurado (SQL).</span><span class="sxs-lookup"><span data-stu-id="0e5d2-108">The **ExecuteSQLQuery** method also returns a record set of results but requires the exact Structured Query Language (SQL) command to be passed in.</span></span> <span data-ttu-id="0e5d2-109">La mayoría de los escenarios deben usar **ExecuteQuery** .</span><span class="sxs-lookup"><span data-stu-id="0e5d2-109">**ExecuteQuery** should be used in most scenarios.</span></span>

## <a name="regular-queries"></a><span data-ttu-id="0e5d2-110">Consultas regulares</span><span class="sxs-lookup"><span data-stu-id="0e5d2-110">Regular Queries</span></span>

<span data-ttu-id="0e5d2-111">Las consultas normales se escriben en el cuadro de entrada de WDS por parte del usuario, incluida la [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md).</span><span class="sxs-lookup"><span data-stu-id="0e5d2-111">Regular queries are those typed into the WDS input box by the user including all [Advanced Query Syntax](-search-2x-wds-aqsreference.md).</span></span> <span data-ttu-id="0e5d2-112">La consulta se pasa a **ExecuteQuery** junto con las columnas de [esquema](-search-2x-wds-schematable.md) de WDS 2. x que se van a devolver, la columna y el orden en que se ordenarán los resultados y las cláusulas para restringir los resultados.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-112">The query is passed to **ExecuteQuery** along with the WDS 2.x [schema](-search-2x-wds-schematable.md) columns to return, the column and order to sort results, and any clauses to restrict results by.</span></span>

<span data-ttu-id="0e5d2-113">El método tiene el formato:</span><span class="sxs-lookup"><span data-stu-id="0e5d2-113">The method has the form:</span></span>

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| <span data-ttu-id="0e5d2-114">Dirección</span><span class="sxs-lookup"><span data-stu-id="0e5d2-114">Direction</span></span> | <span data-ttu-id="0e5d2-115">Variable</span><span class="sxs-lookup"><span data-stu-id="0e5d2-115">Variable</span></span>           | <span data-ttu-id="0e5d2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e5d2-116">Description</span></span>                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5d2-117">En</span><span class="sxs-lookup"><span data-stu-id="0e5d2-117">In</span></span>        | <span data-ttu-id="0e5d2-118">lpcwstrQuery</span><span class="sxs-lookup"><span data-stu-id="0e5d2-118">lpcwstrQuery</span></span>       | <span data-ttu-id="0e5d2-119">El texto de la consulta.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-119">The query text.</span></span> <span data-ttu-id="0e5d2-120">Esta consulta es la misma que una consulta escrita en el cuadro de texto Buscar en la interfaz de usuario de búsqueda en el escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-120">This query is the same as a query typed into the search text box in the Windows Desktop Search user interface.</span></span> <br/> <span data-ttu-id="0e5d2-121">Por ejemplo: `"from:Zara dinner plans"`</span><span class="sxs-lookup"><span data-stu-id="0e5d2-121">For example: `"from:Zara dinner plans"`</span></span><br/> |
| <span data-ttu-id="0e5d2-122">En</span><span class="sxs-lookup"><span data-stu-id="0e5d2-122">In</span></span>        | <span data-ttu-id="0e5d2-123">lpcwstrColumn</span><span class="sxs-lookup"><span data-stu-id="0e5d2-123">lpcwstrColumn</span></span>      | <span data-ttu-id="0e5d2-124">Columnas que se van a incluir, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-124">The columns to include, separated by commas.</span></span> <br/> <span data-ttu-id="0e5d2-125">Por ejemplo: `"DocTitle, Url"`</span><span class="sxs-lookup"><span data-stu-id="0e5d2-125">For example: `"DocTitle, Url"`</span></span><br/>                                                                                            |
| <span data-ttu-id="0e5d2-126">En</span><span class="sxs-lookup"><span data-stu-id="0e5d2-126">In</span></span>        | <span data-ttu-id="0e5d2-127">lpcwstrSort</span><span class="sxs-lookup"><span data-stu-id="0e5d2-127">lpcwstrSort</span></span>        | <span data-ttu-id="0e5d2-128">Columna de invalidación por la que se va a ordenar seguido de ASC para ascendente o DESC en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-128">The Override Column to sort by followed by ASC for ascending or DESC for descending.</span></span> <br/> <span data-ttu-id="0e5d2-129">Por ejemplo: `"LastAuthor DESC"`</span><span class="sxs-lookup"><span data-stu-id="0e5d2-129">For example: `"LastAuthor DESC"`</span></span><br/>                                                  |
| <span data-ttu-id="0e5d2-130">En</span><span class="sxs-lookup"><span data-stu-id="0e5d2-130">In</span></span>        | <span data-ttu-id="0e5d2-131">lpcwstrRestriction</span><span class="sxs-lookup"><span data-stu-id="0e5d2-131">lpcwstrRestriction</span></span> | <span data-ttu-id="0e5d2-132">Restricciones para anexar a través de las cláusulas WHERE en la búsqueda de escritorio de Windows seleccione.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-132">Restrictions to append through WHERE clauses in the Windows Desktop Search select.</span></span> <br/> <span data-ttu-id="0e5d2-133">Por ejemplo: `"Contains(LastAuthor, 'Bill')"`</span><span class="sxs-lookup"><span data-stu-id="0e5d2-133">For example: `"Contains(LastAuthor, 'Bill')"`</span></span><br/>                                       |
| <span data-ttu-id="0e5d2-134">Fuera</span><span class="sxs-lookup"><span data-stu-id="0e5d2-134">Out</span></span>       | <span data-ttu-id="0e5d2-135">ppiRs</span><span class="sxs-lookup"><span data-stu-id="0e5d2-135">ppiRs</span></span>              | <span data-ttu-id="0e5d2-136">El conjunto de registros resultante</span><span class="sxs-lookup"><span data-stu-id="0e5d2-136">The resulting record set</span></span><br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a><span data-ttu-id="0e5d2-137">Consultas SQL</span><span class="sxs-lookup"><span data-stu-id="0e5d2-137">SQL Queries</span></span>

<span data-ttu-id="0e5d2-138">El método **ISearchDesktop.ExecuteSQLQuery** se usa para enviar consultas directas de la base de datos WDS.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-138">The **ISearchDesktop.ExecuteSQLQuery** method is used to send direct WDS database queries.</span></span> <span data-ttu-id="0e5d2-139">La sintaxis de las consultas es similar a la que se usa para SharePoint Server, junto con la capacidad de usar cláusulas SQL GROUP BY de estilo monarca.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-139">The syntax for the queries is similar to that used for SharePoint Server, along with the ability to use Monarch-style SQL GROUP BY clauses.</span></span> <span data-ttu-id="0e5d2-140">La consulta se ejecuta en el índice exactamente como se pasa sin ningún procesamiento adicional de la sintaxis de consulta avanzada a medida que lo hace la API ExecuteQuery.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-140">The query is executed against the index exactly as it is passed in with no additional processing of Advanced Query Syntax as the ExecuteQuery API does.</span></span>

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

<span data-ttu-id="0e5d2-141">El método tiene el formato:</span><span class="sxs-lookup"><span data-stu-id="0e5d2-141">The method has the form:</span></span>

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| <span data-ttu-id="0e5d2-142">Dirección</span><span class="sxs-lookup"><span data-stu-id="0e5d2-142">Direction</span></span> | <span data-ttu-id="0e5d2-143">Variable</span><span class="sxs-lookup"><span data-stu-id="0e5d2-143">Variable</span></span>   | <span data-ttu-id="0e5d2-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e5d2-144">Description</span></span>                                    |
|-----------|------------|------------------------------------------------|
| <span data-ttu-id="0e5d2-145">En</span><span class="sxs-lookup"><span data-stu-id="0e5d2-145">In</span></span>        | <span data-ttu-id="0e5d2-146">lpcwstrSQL</span><span class="sxs-lookup"><span data-stu-id="0e5d2-146">lpcwstrSQL</span></span> | <span data-ttu-id="0e5d2-147">Consulta SQL que se va a ejecutar en el índice de WDS</span><span class="sxs-lookup"><span data-stu-id="0e5d2-147">The SQL query to execute against the WDS index</span></span> |
| <span data-ttu-id="0e5d2-148">Fuera</span><span class="sxs-lookup"><span data-stu-id="0e5d2-148">Out</span></span>       | <span data-ttu-id="0e5d2-149">ppiRs</span><span class="sxs-lookup"><span data-stu-id="0e5d2-149">ppiRs</span></span>      | <span data-ttu-id="0e5d2-150">El conjunto de registros resultante</span><span class="sxs-lookup"><span data-stu-id="0e5d2-150">The resulting record set</span></span>                       |



 

<span data-ttu-id="0e5d2-151">Recursos:</span><span class="sxs-lookup"><span data-stu-id="0e5d2-151">Resources:</span></span>

-   <span data-ttu-id="0e5d2-152">Archivos de compatibilidad para la interfaz ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip</span><span class="sxs-lookup"><span data-stu-id="0e5d2-152">Support files for the ISearchDesktop interface: https://addins.msn.com/support/WDSSDK.zip</span></span>
-   <span data-ttu-id="0e5d2-153">Ejemplo de C# de ISearchDesktop: https://addins.msn.com/support/WDSSample.zip</span><span class="sxs-lookup"><span data-stu-id="0e5d2-153">ISearchDesktop C# Sample: https://addins.msn.com/support/WDSSample.zip</span></span>

## <a name="sample-c-code"></a><span data-ttu-id="0e5d2-154">Código de C++ de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e5d2-154">Sample C++ Code</span></span>

> [!Note]
>
> <span data-ttu-id="0e5d2-155">ESTE CÓDIGO E INFORMACIÓN SE PROPORCIONA "TAL CUAL" SIN GARANTÍA DE NINGÚN TIPO, YA SEA EXPRESA O IMPLÍCITA, INCLUIDAS, ENTRE OTRAS, LAS GARANTÍAS IMPLÍCITAS DE COMERCIABILIDAD O IDONEIDAD PARA UN PROPÓSITO DETERMINADO.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-155">THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.</span></span>
>
> <span data-ttu-id="0e5d2-156">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-156">Copyright (C) Microsoft.</span></span> <span data-ttu-id="0e5d2-157">Todos los derechos reservados.</span><span class="sxs-lookup"><span data-stu-id="0e5d2-157">All rights reserved.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="0e5d2-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e5d2-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0e5d2-159">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0e5d2-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e5d2-160">Sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="0e5d2-160">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="0e5d2-161">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="0e5d2-161">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="0e5d2-162">Llamar a WDS desde páginas web</span><span class="sxs-lookup"><span data-stu-id="0e5d2-162">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

