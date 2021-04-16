---
title: Procesar los resultados de la búsqueda
description: Después de la primera llamada a IDirectorySearch GetFirstRow o IDirectorySearch GetNextRow, s \_ OK, s \_ ADS \_ NoMore \_ Rows o se devuelve un resultado de error.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Procesando anuncio de resultados de búsqueda
- Active Directory, buscar y procesar los resultados de la búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732128438162f5ee8f6fe75bb4d2ce53e0d43070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656329"
---
# <a name="processing-the-search-results"></a>Procesar los resultados de la búsqueda

Después de la primera llamada a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), **s \_ OK**, **s \_ ADS \_ NoMore \_ Rows** o se devuelve un resultado de error.

Si el valor devuelto es un número de **\_ \_ \_ filas** de los anuncios, no se encontraron más objetos que coincidan con el filtro. Si se devuelve un resultado de error, se produce un error en la consulta. En ambos casos, no es necesario procesar las filas del resultado porque no se devolvió nada.

Si **se \_** devuelve, se recupera una fila. Puede analizar las columnas por nombre mediante [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). El nombre es el **lDAPDisplayName** del atributo en la columna. El parámetro pAttributeNames del método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) definió el conjunto de todas las columnas. Si se especifica **null** , el conjunto de todas las columnas es la Unión de todas las propiedades que se encuentran para todos los objetos devueltos. Para leer el conjunto completo de columnas devueltas para un objeto, use [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) para recorrer en iteración cada columna y use el nombre de columna devuelto para llamar a **IDirectorySearch:: getcolumn (**.

El método [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) devuelve una estructura de [**columnas de \_ búsqueda \_ de ADS**](/windows/desktop/api/iads/ns-iads-ads_search_column) que contiene el nombre del atributo, el tipo de atributo, el recuento de valores y un puntero a una matriz de estructuras [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que contienen los valores. Puede recorrer las estructuras **ADSVALUE** para leer los valores de la propiedad devuelta por la columna. Debe leer el miembro adecuado de la estructura **ADSVALUE** basándose en el [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) especificado por el miembro **dwADsType** de la estructura de **\_ \_ columnas de búsqueda ADS** (o el miembro **dwType** de la estructura **ADSVALUE** ). Por ejemplo, si **dwADsType** era **ADSTYPE \_ Integer**, leería el miembro **entero** de cada estructura **ADSVALUE** .

Para obtener más información y un ejemplo de código, consulte el [código de ejemplo para buscar usuarios](example-code-for-searching-for-users.md).

 

 